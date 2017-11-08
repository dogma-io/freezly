# freezly

Small utility for deeply freezing objects in JavaScript.

## Installation

**npm**

```bash
npm install freezly
```

**yarn**

```bash
yarn add freezly
```

## Usage

The most basic usage is achieved with the following command, replacing the source path with the path to your source code to transform and the output path with the path to where you want the transformed code to be written.

```js
import deepFreeze from 'freezly'

const frozenObject = deepFreeze({
  foo: ['bar'],
})

// The following will throw an error as you can't mutate frozen objects
frozenObject.baz = 'spam' // Can't add properties to frozen object
frozenObject.foo.push('baz') // Can't push items to frozen array
```
