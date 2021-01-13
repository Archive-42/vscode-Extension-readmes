# turbo-js

Turbo-js for vscode is forked from [atom-turbo-javascript](https://github.com/extrabacon/atom-turbo-javascript)

### Declarations

#### `l=⇥` let assignment
```js
let ${1:name} = ${2:value}
```

#### `co⇥` const statement
```js
const ${1:name}
```

#### `co=⇥` const assignment
```js
const ${1:name} = ${2:value}
```

### Flow Control

#### `if⇥` if statement
```js
if (${1:condition}) {
  ${0}
}
```

#### `ife⇥` else statement
```js
if (${1:condition}) {
  ${0}
} else {

}
```

#### `fo⇥` for of loop (ES6)
```js
for (let ${1:key} of ${2:source}) {
  ${0}
}
```

#### `wl⇥` while loop
```js
while (${1:condition}) {
  ${0}
}
```

#### `tc⇥` try/catch
```js
try {
 ${0}
} catch (${1:err}) {

}
```

### Functions

#### `fn⇥` named function
```js
function ${1:name}(${2:arguments}) {
  ${0}
}
```

#### `iife⇥` immediately-invoked function expression (IIFE)
```js
(function (${1:arguments}) {
  ${0}
})(${2});
```

#### `af⇥` arrow function (ES6)
```js
(${1:arguments}) => ${2:statement}
```

#### `afb⇥` arrow function with body (ES6)
```js
(${1:arguments}) => {
\t${0}
}
```

### Iterables

#### `fe⇥` forEach loop (chainable)
```js
${1:iterable}.forEach((${2:item}) => {
  ${0}
});
```

#### `reduce⇥` reduce function (chainable)
```js
${1:iterable}.reduce((${2:previous}, ${3:current}) => {
  ${0}
}${4:, initial});
```

#### `filter⇥` filter function (chainable)
```js
${1:iterable}.filter((${2:item}) => {
  ${0}
});
```

#### `find⇥` ES6 find function (chainable)
```js
${1:iterable}.find((${2:item}) => {
  ${0}
});
```

### Objects and classes

#### `cls⇥` class (ES6)
```js
class ${1:name} {
  constructor(${2:arguments}) {
    ${0}
  }
}
```

#### `cex⇥` child class (ES6)
```js
class ${1:name} extends ${2:base} {
  constructor(${2:arguments}) {
    super(${2:arguments});
    ${0}
  }
}
```

#### `med⇥` method (ES6 syntax)
```js
${1:method}(${2:arguments}) {
  ${0}
}
```

#### `get⇥` getter (ES6 syntax)
```js
get ${1:property}() {
  ${0}
}
```

#### `set⇥` setter (ES6 syntax)
```js
set ${1:property}(${2:value}) {
  ${0}
}
```

#### `proto⇥` prototype method (chainable)
```js
${1:Class}.prototype.${2:methodName} = function (${3:arguments}) {
  ${0}
};
```

#### `oa⇥` Object assign
```js
Object.assign(${1:dest}, ${2:source})
```

#### `ok⇥` Object.keys
```js
Object.keys(${1:obj})
```

### Promises

#### `rp⇥` return Promise (ES6)
```js
return new Promise((resolve, reject) => {
  ${0}
});
```

### ES6 modules

#### `ex⇥` module export
```js
export ${1:member};
```

#### `exd⇥` module default export
```js
export default ${1:member};
```

#### `im⇥` module import
```js
import ${1:*} from '${2:module}';
```

#### `ima⇥` module import as
```js
import ${1:*} as ${2:name} from '${3:module}';
```

### Console

#### `cl⇥` console.log
```js
console.log(${0});
```

#### `ce⇥` console.error
```js
console.error(${0});
```

#### `cw⇥` console.warn
```js
console.warn(${0});
```

### Timers

#### `st⇥` setTimeout
```js
setTimeout(() => {
  ${0}
}, ${1:delay});
```

#### `si⇥` setInterval
```js
setInterval(() => {
  ${0}
}, ${1:delay});
```

#### `sim⇥` setImmediate
```js
setImmediate(() => {
  ${0}
});
```

### Node.js specifics

#### `re⇥` require a module
```js
require('${1:module}');
```

#### `cre⇥` require a module
```js
const ${1:name} = require('${2:module}');
```

#### `me⇥` module.exports
```js
module.exports = ${1:name};
```

### Miscellaneous

#### `us⇥` use strict
```js
'use strict';
```