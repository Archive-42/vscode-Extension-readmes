# 个人框架 db文件扩展

## db文件说明

db文件用于将nodejs中的sql代码统统提取出来，放到一个db文件中，以避免代码的混乱。

db文件中使用"##"表示注释，使用"#"表示名称。

db文件中，每个SQL语句之前必须有一个名称。

db文件中的SQL语句支持换行。

## 特别说明

db文件属于是自定义文件，如果想在项目中使用，需要为db文件写一个解析器。

下面是JavaScript的一种简单实现方法。

```javascript
/**
 * db文件解析器
 * 此解析器用于解析db文件并将db文件中的SQL语句存放到全局变量sql中。
 * 架设db文件所在目录的结构如下：
 * 		dbFiles
 * 			|	user.db
 * 			|	group.db
 * 经过解析之后，sql变量结构如下：
 * 		{
 * 			user:{
 * 				//sql名称 => sql语句
 * 			},
 * 			group:{
 * 				//sql名称 => sql语句
 * 			}
 * 		}
 * db文件格式如下：
 * 		## 注释
 * 		# sql名称
 * 		sql语句
 */


const fs = require('fs')
const path = require('path')

//用于存放SQL语句
global.sql = {};

//转换SQL语句
function parseSql(content = '') {
	let obj = {};
	//去掉注释
	content = content.replace(/^##[\s\S]+?\n/gim, '');
	//以#号分割
	content.split(/#/gim)
		//去掉每个字符串前后的空白
		.map(str => str.trim())
		//过滤空字符串
		.filter(str => !!str)
		//以换行分割每个字符串
		.map(str => str.split(/\n+/))
		//组合成对象并返回
		.forEach(([key, ...values]) => obj[key.trim()] = values.join('\n'));
	//返回转换结果
	return obj;
}

//将SQL文件内容进行解析，并将解析结果存放到全局。
function makeSqlData(filename, content) {
	//去除后缀得到名称作为变量名
	let [_, name] = filename.split(/^([\s\S]+?).db/);
	//解析sql内容
	global.sql[name] = parseSql(content + '');
}

//db文件加载器
module.exports = function loadDBFile() {
	//这里配置一下db文件所在的文件夹，该文件夹下的所有db文件都会被解析并存放到全局变量sql中。
	let dbFilePath = path.join(__dirname, './../config/sql');
	//读取文件列表
	fs.readdirSync(dbFilePath).forEach(file => {
		//如果不是以db结尾的文件则不进行处理
		if (!/.db$/.test(file)) return;
		//读取文件并处理
		let filePath = path.join(dbFilePath, file);
		let content = fs.readFileSync(filePath);
		//处理内容
		makeSqlData(file, content);
	})
}
```


## db文件格式如下

```
## 使用此语句可以添加一个用户到用户表中
# createUser
insert into `user` set ?

## 使用此语句可以修改用户信息
# updateUser
update `user` set ? where `id` = ?
```
