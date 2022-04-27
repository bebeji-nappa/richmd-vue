# richmd-vue
![NPM](https://img.shields.io/npm/l/richmd-vue)
![npm](https://img.shields.io/npm/v/richmd-vue)
![NPM](https://img.shields.io/npm/dw/richmd-vue)


## Install
```
yarn add richmd richmd-vue
```

## Usage
It use `Richmd` component`.

```js
<template>
  <div>Welcome to my Vue app!</div>
  <Richmd :text="text" :className="hoge" />
</template>
<script>
import Richmd from "richmd-vue"
const md = `# aaa
bbb
ccc

===info
test
===
`;
export default {
  components: {
    Richmd,
  },
  data() {
    return {
      text: md,
      hoge: "hoge"
    };
  },
};
</script>
<style>
@import './node_modules/richmd/richmd.css';
</style>
```

## Props
| Name | Description |
| --- | --- |
| `text` | To parse HTML set Markdown text. |
| `id` | It set id. |
| `className` | It set ClassName. |

## License
MIT
