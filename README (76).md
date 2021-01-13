# Short JS Doc  
   Short Javascript Snippets and Documentation based on JSDuck.  
 A collection of Javascript snippets for faster developmment in Visual Studio Code Based on JsDuck Ducumentation implenting for Sencha Ext JS. 
# Content:  

- [Access object property](#access-object-property)
- [Array property](#array-property)
- [Author information](#author-information)
- [Bind configuration](#bind-configuration)
- [Bind property](#bind-property)
- [Comment code](#comment-code)
- [Console debug block](#console-debug-block)
- [Call function](#call-function)
- [Console methods](#console-methods)
- [Copyright Tag](#copyright-tag)
- [Context tag](#context-tag)
- [Control variables](#control-variables)
- [Deprecated Tag](#deprecated-tag)
- [Ext JS Class definition](#ext-js-class-definition)
- [Equal name property and value](#equal-name-property-and-value)
- [Ext widget](#ext-widget)
- [Function property](#function-property)
- [Get property](#get-property)
- [Generic Tag](#generic-tag)
- [Justification change](#justification-change)
- [Method property](#method-property)
- [Object property](#object-property)
- [Property definition](#property-definition)
- [Property](#property)
- [Property tag](#property-tag)
- [Set and get property](#set-and-get-property)
- [String property](#string-property)
- [Todo Tag](#todo-tag)
- [Update function property](#update-function-property)
- [Version Tag](#version-tag)
- [Ext log](#ext-log)


# Example:  

## Access object property
### `aop + tab` 
```
${1:object}[${2:'${3:property}'}];
``` 

## Array property
### `ap + tab` 
```
${1:name}${2|:,=|} [${3}]${4:,}
``` 

## Author information
### `at + tab` 
```
/*!
 * @author ${1:user} <${2:email}>
 * date ${CURRENT_MONTH}/${CURRENT_DATE}/${CURRENT_YEAR}
 * ${3:description} $0
 */
``` 

## Bind configuration
### `bc + tab` 
```
${1:bind}: {
  ${2:property}: '{${3:value}}',$0
},
``` 

## Bind property
### `bp + tab` 
```
${1:property}: '{${2:value}}'${3:,}
``` 

## Comment code
### `cc + tab` 
```
/**
 * $0
 */
``` 

## Console debug block
### `cd + tab` 
```
//<debug>
${1}
console.${2|log,info,warn,error|}('${3:debug}', ${4:arguments}); $0
//</debug>
``` 

## Call function
### `cf + tab` 
```
${1:function}($0);
``` 

## Console methods
### `cm + tab` 
```
//<debug>
${1}
  console.${2|assert,count,debug,dir,dirxml,error,group,groupCollapsed,groupEnd,info,log,profile,profileEnd,table,time,timeEnd,timeStamp,trace,warn|}(${4:arguments}); $0
//</debug>
``` 

## Copyright Tag
### `crt + tab` 
```
/**
 * @copyright  ${1:name} ${2:year} 
 * $0 
 */
``` 

## Context tag
### `ct + tab` 
```
@${1|private,protected,public|} ${2:args}
``` 

## Control variables
### `cv + tab` 
```
var ${1:me} = this,
  ${2:view} = ${1:me}.getView(),
  ${3:model} = ${1:me}.getViewModel(),
  ${4:refs} = ${1:me}.getReferences();
  $0
``` 

## Deprecated Tag
### `dt + tab` 
```
/**
 * @deprecated ${CURRENT_MONTH}/${CURRENT_DATE}/${CURRENT_YEAR} $0 
 */
``` 

## Ext JS Class definition
### `ed + tab` 
```
/**
 * @class ${1:name}
 * @extends ${2:extend}
 * @xtype ${4:xtype}
 * ${5:description}
 */
Ext.define('${1:name}', {
  extend: '${2:extend}',
  xtype: '${4:xtype}',
  ${6://}requires: [${7}],
  initComponent: function (){
    var ${8:me} = this;

    Ext.apply(${8:me}, {
      items: [
       {
        $0
       }
      ]
    });

    ${8:me}.callParent(arguments);
  }
});
``` 

## Equal name property and value
### `ep + tab` 
```
${1:property}${2|:,=|} ${3}${4:property} ${5:,}
``` 

## Ext widget
### `ew + tab` 
```
Ext.${1|widget,create|}('${xtype}',{
  $0
});
``` 

## Function property
### `fp + tab` 
```
/**
 * ${1:name} ${2:description}
 * @${3|private,protected,public|}
 */
${1:name}${4|:,=|} function (${5}) {
  $0
},
``` 

## Get property
### `gp + tab` 
```
${1:property}${2|:,=|} ${3:model}.${4:get}('${5:dataIndex}')${6:,}
``` 

## Generic Tag
### `gt + tab` 
```
/**
 * @${1:tag} $0 
 */
``` 

## Justification change
### `jc + tab` 
```
/*
 * ${1:user} ${CURRENT_MONTH}/${CURRENT_DATE}/${CURRENT_YEAR} ${2:justification} $0
 */
``` 

## Method property
### `mp + tab` 
```
/**
 * @${1|method,function|} ${2:name} ${3:description}
 * @returns {${4|String,Number,Boolean,Object,Array,Function,Date|}} ${5:property} `${6:default}` ${7:description}
 * @${8|private,protected,public|}
 */
${2:name} ${9|:,=|} function (${10}) {
  var ${5:property} = ${6:null};
  $0
  return ${5:property};
},
``` 

## Object property
### `op + tab` 
```
${1:name}${2::} {
  ${4:property}: ${5:''}, $0
},
``` 

## Property definition
### `pd + tab` 
```
/*
 * @${1|cfg,arg,argument|} {${2|String,Number,Boolean,Object,Array,Function,Date|}${3}} ${4:name}  `${5:default}` ${6:description}
 */
${4:name}${7|:,=|} ${5:null}${8:,}
``` 

## Property
### `pp + tab` 
```
${1:property}${2|:,=|} ${3:null}${4:,}
``` 

## Property tag
### `pt + tab` 
```
@${1|param,arg,argument|} {${2|String,Number,Boolean,Object,Array,Function,Date|}${3}} ${4:name}  `${5:default}` ${6:description}
``` 

## Set and get property
### `sg + tab` 
```
/**
 * @param {${1:type}} ${2:name}  `${3:default}` ${4:description} 
 * @${5|public,private,protected|}
 */
set${6:Property}${7|:,=|} function (${2:name}) {
  var old${2:name} = this.${2:name};
  if (${2:name} !== old${2:name}) {
    ${8}
    this.${2:name} = ${2:name};
    //this.update${6:Property}(${2:name}, old${2:name});
  }
},
/**
 * @returns {${1:type}} ${2:name} `${3:default}` ${4:description} 
 * @${5|public,private,protected|}
 */
get${6:Property}${7|:,=|} function () {
  var ${2:name} = this.${2:name} || ${3:default};
  ${9}
  return ${2:name};
},
``` 

## String property
### `sp + tab` 
```
${1:property}${2|:,=|} '${3:value}'${4:,}
``` 

## Todo Tag
### `td + tab` 
```
/**
 * @todo ${1:description} $0
 */
``` 

## Update function property
### `uf + tab` 
```
 /**
  * @${1|private,protected,public|}
  */
update${2:Property} ${3|:,=|} function (new${2:Property}, old${2:Property}) {
  $0
},
``` 

## Version Tag
### `vt + tab` 
```
/**
 * @version ${1:major}.${2:minor}.${3:patch} $0
 */
``` 

## Ext log
### `xl + tab` 
```
${Ext}.log({
  msg: '${1:debug}',
  level: '${2|log,info,error,warn|}',
  dump: ${3:arguments},
  stack: ${4|true,false|}
});
``` 

