# 📝 VS Code JavaScript snippets

[![Version](https://vsmarketplacebadge.apphb.com/version/runningcoder.js-snippets.svg)](https://vsmarketplacebadge.apphb.com/version/runningcoder.js-snippets.svg)

This extension provides you JavaScript snippets for [VS Code](https://code.visualstudio.com/)

## 📚 Supported languages (file extensions)

* html (.html)
* JavaScript (.js)
* JavaScript React (.jsx)
* TypeScript (.ts)
* TypeScript React (.tsx)

## 📖 Snippets

Below is a list of all available snippets and the triggers of each one. The `⇥` means the `TAB` key.

### Console

<table>
<thead>
<tr>
  <th>

**trigger**

  </th>
  <th>

**snippet(JS)**

  </th>
  <th>

**snippet(TS)**

  </th>
</tr>
</thead>
<tbody>
<tr>
  <td><code>ca⇥</code></td>
  <td>   

```js
console.assert(condition, message)
```

  </td>
  <td>   

```ts
console.assert(condition, message)
```

  </td>
</tr>

<tr>
  <td><code>ccl⇥</code></td>
  <td>   

```js
console.clear()
```

  </td>
  <td>   

```ts
console.clear()
```

  </td>
</tr>

<tr>
  <td><code>cc⇥</code></td>
  <td>   

```js
console.count(label)
```

  </td>
  <td>   

```ts
console.count(label)
```

  </td>
</tr>

<tr>
  <td><code>ccr⇥</code></td>
  <td>   

```js
console.countReset(label)
```

  </td>
  <td>   

```ts
console.countReset(label)
```

  </td>
</tr>

<tr>
  <td><code>cdb⇥</code></td>
  <td>   

```js
console.debug(message)
```

  </td>
    <td>   

```ts
console.debug(message)
```

  </td>
</tr>

<tr>
  <td><code>cd⇥</code></td>
  <td>   

```js
console.dir(value)
```

  </td>
  <td>   

```ts
console.dir(value)
```

  </td>
</tr>

<tr>
  <td><code>cdx⇥</code></td>
  <td>   

```js
console.dirxml(object)
```

  </td>
  <td>   

```ts
console.dirxml(object)
```

  </td>
</tr>

<tr>
  <td><code>ce⇥</code></td>
  <td>   

```js
console.error(message)
```

  </td>
  <td>   

```ts
console.error(message)
```

  </td>
</tr>

<tr>
  <td><code>cg⇥</code></td>
  <td>   

```js
console.group(groupTitle)
```

  </td>
  <td>   

```ts
console.group(groupTitle)
```

  </td>
</tr>

<tr>
  <td><code>cgc⇥</code></td>
  <td>   

```js
console.groupCollapsed(groupTitle)
```

  </td>
  <td>   

```ts
console.groupCollapsed(groupTitle)
```

  </td>
</tr>

<tr>
  <td><code>cge⇥</code></td>
  <td>   

```js
console.groupEnd()
```

  </td>
  <td>   

```ts
console.groupEnd()
```

  </td>
</tr>

<tr>
  <td><code>ci⇥</code></td>
  <td>   

```js
console.info(message)
```

  </td>
  <td>   

```ts
console.info(message)
```

  </td>
</tr>

<tr>
  <td><code>cl⇥</code></td>
  <td>   

```js
console.log(message)
```

  </td>
  <td>   

```ts
console.log(message)
```

  </td>
</tr>

<tr>
  <td><code>ctb⇥</code></td>
  <td>   

```js
console.table(tabularData)
```

  </td>
  <td>   

```ts
console.table(tabularData)
```

  </td>
</tr>


<tr>
  <td><code>ct⇥</code></td>
  <td>   

```js
console.time(label)
```

  </td>
  <td>   

```ts
console.time(label)
```

  </td>
</tr>

<tr>
  <td><code>cte⇥</code></td>
  <td>   

```js
console.timeEnd(label)
```

  </td>
  <td>   

```ts
console.timeEnd(label)
```

  </td>
</tr>

<tr>
  <td><code>ctr⇥</code></td>
  <td>   

```js
console.trace(message)
```

  </td>
  <td>   

```ts
console.trace(message)
```

  </td>
</tr>



<tr>
  <td><code>cw⇥</code></td>
  <td>   

```js
console.warn(message)
```

  </td>
  <td>   

```ts
console.warn(message)
```

  </td>
</tr>


</tbody>
</table>

### Array

<table>
<thead>
<tr>
  <th>

**trigger**

  </th>
  <th>

**snippet(JS)**

  </th>
  <th>

**snippet(TS)**

  </th>
</tr>
</thead>
<tbody>
<tr>
  <td><code>Af⇥</code></td>
  <td>   

```js
Array.from(arrayLike, mapFn)
```

  </td>
  <td>   

```ts
Array.from(arrayLike, mapFn)
```

  </td>
</tr>

<tr>
  <td><code>Aia⇥</code></td>
  <td>   

```js
Array.isArray(value)
```

  </td>
  <td>   

```ts
Array.isArray(value)
```

  </td>
</tr>

<tr>
  <td><code>Ao⇥</code></td>
  <td>   

```js
Array.of(items)
```

  </td>
  <td>   

```ts
Array.of(items)
```

  </td>
</tr>

<tr>
  <td><code>.concat⇥</code></td>
  <td>   

```js
.concat(items)
```

  </td>
  <td>   

```ts
.concat(items)
```

  </td>
</tr>

<tr>
  <td><code>.copyWithin⇥</code></td>
  <td>   

```js
.copyWithin(target, start, end)
```

  </td>
    <td>   

```ts
.copyWithin(target, start, end)
```

  </td>
</tr>

<tr>
  <td><code>.entries</code></td>
  <td>   

```js
.entries()
```

  </td>
    <td>   

```ts
.entries()
```

  </td>
</tr>

<tr>
  <td><code>.every</code></td>
  <td>   

```js
.every((value, index, array) => {})
```

  </td>
    <td>   

```ts
.every((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.fill</code></td>
  <td>   

```js
.fill(target, start, end)
```

  </td>
    <td>   

```ts
.fill(target, start, end)
```

  </td>
</tr>

<tr>
  <td><code>.filter</code></td>
  <td>   

```js
.filter((value, index, array) => {})
```

  </td>
    <td>   

```ts
.filter((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.find</code></td>
  <td>   

```js
.find((value, index, array) => {})
```

  </td>
    <td>   

```ts
.find((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.findIndex</code></td>
  <td>   

```js
.findIndex((value, index, array) => {})
```

  </td>
    <td>   

```ts
.findIndex((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.flat</code></td>
  <td>   

```js
.flat(depth)
```

  </td>
    <td>   

```ts
.flat(depth)
```

  </td>
</tr>

<tr>
  <td><code>.flatMap</code></td>
  <td>   

```js
.flatMap((value, index, array) => {})
```

  </td>
    <td>   

```ts
.flatMap((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.forEach</code></td>
  <td>   

```js
.forEach((value, index, array) => {})
```

  </td>
    <td>   

```ts
.forEach((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.includes</code></td>
  <td>   

```js
.includes(searchElement, fromIndex)
```

  </td>
    <td>   

```ts
.includes(searchElement, fromIndex)
```

  </td>
</tr>

<tr>
  <td><code>.indexOf</code></td>
  <td>   

```js
.indexOf(searchElement, fromIndex)
```

  </td>
    <td>   

```ts
.indexOf(searchElement, fromIndex)
```

  </td>
</tr>

<tr>
  <td><code>.join</code></td>
  <td>   

```js
.join(separator)
```

  </td>
    <td>   

```ts
.join(separator)
```

  </td>
</tr>

<tr>
  <td><code>.keys</code></td>
  <td>   

```js
.keys()
```

  </td>
    <td>   

```ts
.keys()
```

  </td>
</tr>

<tr>
  <td><code>.lastIndexOf</code></td>
  <td>   

```js
.lastIndexOf(searchElement, fromIndex)
```

  </td>
    <td>   

```ts
.lastIndexOf(searchElement, fromIndex)
```

  </td>
</tr>

<tr>
  <td><code>.map</code></td>
  <td>   

```js
.map((value, index, array) => {})
```

  </td>
    <td>   

```ts
.map((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.pop</code></td>
  <td>   

```js
.pop()
```

  </td>
    <td>   

```ts
.pop()
```

  </td>
</tr>

<tr>
  <td><code>.push</code></td>
  <td>   

```js
.push(value)
```

  </td>
    <td>   

```ts
.push(value)
```

  </td>
</tr>

<tr>
  <td><code>.reduce</code></td>
  <td>   

```js
.reduce((previousValue, currentValue, currentIndex, array) => {}, initialValue)
```

  </td>
    <td>   

```ts
.reduce((previousValue, currentValue, currentIndex, array) => {}, initialValue)
```

  </td>
</tr>

<tr>
  <td><code>.reduceRight</code></td>
  <td>   

```js
.reduceRight((previousValue, currentValue, currentIndex, array) => {}, initialValue)
```

  </td>
    <td>   

```ts
.reduceRight((previousValue, currentValue, currentIndex, array) => {}, initialValue)
```

  </td>
</tr>

<tr>
  <td><code>.reverse</code></td>
  <td>   

```js
.reverse()
```

  </td>
    <td>   

```ts
.reverse()
```

  </td>
</tr>

<tr>
  <td><code>.slice</code></td>
  <td>   

```js
.slice(start, end)
```

  </td>
    <td>   

```ts
.slice(start, end)
```

  </td>
</tr>

<tr>
  <td><code>.some</code></td>
  <td>   

```js
.some((value, index, array) => {})
```

  </td>
    <td>   

```ts
.some((value, index, array) => {})
```

  </td>
</tr>

<tr>
  <td><code>.sort</code></td>
  <td>   

```js
.sort((a, b) => {})
```

  </td>
    <td>   

```ts
.sort((a, b) => {})
```

  </td>
</tr>

<tr>
  <td><code>.unshift</code></td>
  <td>   

```js
.unshift(value)
```

  </td>
    <td>   

```ts
.unshift(value)
```

  </td>
</tr>

<tr>
  <td><code>.values</code></td>
  <td>   

```js
.values()
```

  </td>
    <td>   

```ts
.values()
```

  </td>
</tr>


</tbody>
</table>
