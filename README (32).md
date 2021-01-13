# vscode-js-import
[![Marketplace Version](https://vsmarketplacebadge.apphb.com/version/wangtao0101.vscode-js-import.svg)](https://marketplace.visualstudio.com/items?itemName=wangtao0101.vscode-js-import)
[![Installs](https://vsmarketplacebadge.apphb.com/installs/wangtao0101.vscode-js-import.svg)](https://marketplace.visualstudio.com/items?itemName=wangtao0101.vscode-js-import)
[![Build Status](https://img.shields.io/travis/wangtao0101/vscode-js-import.svg?style=flat)](https://travis-ci.org/wangtao0101/vscode-js-import)
[![Marketplace Version](https://vsmarketplacebadge.apphb.com/trending-monthly/wangtao0101.vscode-js-import.svg)](https://marketplace.visualstudio.com/items?itemName=wangtao0101.vscode-js-import)

Intelligent and fast import extension for js in vscode, support import position option and adding import to existing import statement. !!!

# Multi-root workspace Ready!


# Introduce
![GitHub Logo](https://github.com/wangtao0101/vscode-js-import/blob/master/img/newimport.gif?raw=true)

# Heads up
We have to move shortcut to ctrl + alt + h  (mac cmd + alt + h)!!!

# Shortcuts
ctrl + alt + h  (mac cmd + alt + h)

Move cursor into target word and enter shortcuts, then select the match import.

# Feature
## Support autofix by using eslint rule(no-undef) or ts compiler error

To enable the feature, you should install enable [eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) in vscode or enable ts compiler.

![GitHub Logo](https://github.com/wangtao0101/vscode-js-import/blob/master/img/autofix.gif?raw=true)

## Support import in multiple line and support comment in any where
If origin import statement occupies multiple lines or exceed maxLine option , we will turn into multiple line mode and carefully handle comments.

Here we add a new namedImport 'e':

![GitHub Logo](https://github.com/wangtao0101/vscode-js-import/blob/master/img/mer.png?raw=true)

We split comments into every identifier:
1. Comments in the same line with defaultImport or 'import' word will be moved after '{'.
2. There are two kinds of comment related to namedImports, comments in previous line or in the same line of namedImports, comments in previous will be in previous also, and comments in the same line will be moved after ','
3. Comments in the same line with 'from' word or moduleSpecifier will be moved after ';'

Tips: We don't know how to put the comment of the statement in somewhere after spliting the single line import statement, so we move the comment after moduleSpecifier, then you should move comment to the right position by your self. (comments like eslint-disable-line)

## Suport insert position option
There are two positions we can insert new statement, before all import statements or after all import statements. (soon we can support sort option)

You should know how we deal with comments.
```
// i am leading comment of import a from 'b';
import a from 'b';
// i am trailing comment of import a from 'b';

// i am leading comment of import a from 'b';
import a from 'b';
// i am leading comment of import c from 'd';
import c from 'd';
```
So, if you want to comment after import in a new line, you should not forget to add a empty line after comment.

Also, we can skip @flow or copyright comment.

## Support auto code completion
![GitHub Logo](https://github.com/wangtao0101/vscode-js-import/blob/master/img/codecomplete.gif?raw=true)

## Support import scss, css, less, json, bmp, gif, jpe, jpeg, png ... file, support css-modules
see config js-import.plainFileSuffix and js-import.plainFileSuffixWithDefaultMember

## Support multi-packages like [lerna](https://github.com/lerna/lerna) style
If you have a file system that looks like this:
```
my-lerna-repo/
  package.json
  packages/
    package-1/
      abc.js
      def.js
      package.json
    package-2/
      package.json
```
Then you can config looks like this:
```
"js-import.root": "packages"
"js-import.alias": {
    "package-1": "packages/package-1/"
    "package-2": "packages/package-2/"
}
```
If you you want to import the identifier abc in abc.js, the statement looks like this:
```
import abc from 'package-1/abc'
```
If the target file and source file are in same package, the extension wil use relative path.

## node_modules support

We only process module form dependencies, devDependencies, peerDependencies, optionalDependencies in package.json,
and only extract import from mainfile in module's package.json.

If you want to import module using vscode-js-import,
you should add the module into package.json. Besides, we support export style like module.exports = require('./lib/React');

We will watch the change of package.json, and auto add and remove module.

## A cute icon shows that how many export statements in your workspace.
![GitHub Logo](https://github.com/wangtao0101/vscode-js-import/blob/master/img/icon.png?raw=true)

# Setting
```
//the source dir, currently we only support single root
"js-import.root": "src"

//module alias like webpack resolve.alias 或者 typescript compilerOptions.paths, not support nested alias path, e.g { util: 'src/util/' }
"js-import.alias": {
    "helpalias": "src/package/packageA"
}
//you can import statement from packageA like: import abc from 'helpalias/abc'，import ccc from 'helpalias/xxx/xx'.

//Glob for files to watch and scan, e.g ./src/** ./src/app/**/*.js. Defaults to **/*.{jsx,js,ts,tsx}
"js-import.filesToScan": "**/*.{jsx,js,tsx,ts}"

//Glob for files to exclude from watch and scan, e.g **/.meteor/**. Defaults to nothing
"js-import.excludeFilesToScan": ""

//suffix of plainFiles. Defaults to css,less,sass
//When import file with these suffixes, the import statement only has 'import' and 'model-name' like 'import 'xxx.less'.
//if you use css modules, you can remove css,less,sass in here, see config js-import.plainFileSuffixWithDefaultMember
"js-import.plainFileSuffix": "css,less,sass"

//suffix of plainFiles which should be imported with default member. Defaults to json,bmp,gif,jpe,jpeg,png
//When import file with these suffixes, the import statement has default import like 'import json form 'xxx.json'
//if you use css modules, you can add css,less,sass in here
"js-import.plainFileSuffixWithDefaultMember": "json,bmp,gif,jpe,jpeg,png"

//the insert position of new import statement, first means first of all imports, last means last of all imports, soon we will suport sort
"js-import.insertPosition": "last"

//option for comma-dangle to generate import statement, like esline rule imports of comma-dangle, there are four options :　never, always, always-multiline, only-multiline
"js-import.commaDangleImport": "never"

//whether to enable codeCompletion
"js-import.codeCompletion": true

//whether to use singlequote or use doublequote
"js-import.quote": "singlequote"

//whether to autofix import when you select completion item, you can set it false to avoid mistaken import,
//then we will only provide code completion and you can use shutcut or autofix to import identifier
"js-import.codeCompletionAction": false

//max-line length like eslint rule max-line, the -1 will disable the rule,
//if import statement exceed maxLen, the statement will be split into multiple lines.
"js-import.maxLen": 100

//whether to add semicolon after import statement
"js-import.semicolon": true
```

# TODO
Currently in beta, there are a lot of work to do;
- [x] full suport in node_modules, only extract export form main file and support module.exports = require('./lib/React')
- [x] full support import statement, such as 'feedline' in import statement
- [x] option for insert position (ability to skip flow, Copyright, Lisence comment in top of file)
- [x] support autocomplete
- [x] support auto fix by eslint rule
- [x] support option for max-line like eslint rule max-line, auto split statement to mutilines
- [x] support import "module-name"
- [x] support import scss, css, less, json, bmp, gif, jpe, jpeg, png file
- [ ] sort import statement by eslint rule, deal with comment
- [ ] support shortcut goto module under cursor, spec react conpoment, alias module
- [ ] support commonjs, considering require nodejs built-in modules
- [ ] full support typescript, using typescript parse
- [ ] full support flow, export type and import type
- [ ] support action for remove unused import identifier using eslint or tslint, eslint rule(no-unused-vars)
- [ ] support config for extra module path, such as module in node_modules but not in dependenciess
- [ ] support config for css modules, import less css sass like import * as css from 'xxx.less'
- [ ] support single vue Single File Components
- [ ] support read path of tsconfig.json and alias of webpack.config to config alias

# Export RegExp
```
exports.default\\s*=\\s*(\\w+).default
module.exports\\s*=\\s*(\\w+)
exports\\[[\\'\\"]default[\\'\\"]\\]\\s*=\\s*(\\w+)
export\\s+(default\\s+){0,1}(?:(?:const|let|var|interface|enum|function|function\\*|class|abstract\\sclass)\\s+){0,1}([\\w]+)
exports\\.([\\w]+)\\s*=
exports\\[\\"([\\w]+)\\"\\]\\s*=
Object.defineProperty\\(\\s*exports\\s*,\\s*[\\'|\\"](https://github.com/wangtao0101/vscode-js-import/blob/master/[\\w]+)[\\'|\\"]
export\\s+(?:default\\s+){0,1}(\\{[^\\}]+\\})
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/wangtao0101/vscode-js-import/issues).

# Thanks
some code from [import-js](https://github.com/Galooshi/import-js)

