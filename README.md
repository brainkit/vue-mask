Vue input mask
==============

Simple input mask lib for vue.js based on [PureMask.js](https://github.com/romulobrasil/PureMask.js)

## Installation

This version requires Vue 2.X.

  `npm install vue-mask-directive`

## Usage

```javascript
import Vue     from 'vue'
import VueMaskDirective from 'vue-mask-directive'

/** Activate vue.js plugins **/
Vue.use(VueMaskDirective);
```

Now you are ready to use it in the code!

```html
<input type="text" v-mask="'####-##'" v-model="myInputModel">
<!-- OR -->
<input type="text" v-mask="'##/##/#### ##:##'" v-model="myInputModel">
```
**Notice:** `v-model` is required starting from `v1.1.0`, because [a lot](https://github.com/probil/v-mask/issues/16) [of](https://github.com/probil/v-mask/issues/30) [bugs](https://github.com/probil/v-mask/issues/29) with HTMLElement event listeners and sync with Vue internals.

There is no reason to support using this lib for using without `v-model` but open the door for using on [custom inputs](http://vuejs.org/v2/guide/components.html#Form-Input-Components-using-Custom-Events).

## Format description

List of supported placeholders:

| Value | Format                       |
|-------|------------------------------|
| #     | Number (0-9)                 |
| A     | Letter in any case (a-z,A-Z) |
| N     | Number or letter             |
| X     | Any symbol                   |

## Tests

[Jest](https://github.com/facebook/jest) is used for unit-tests.

You can run tests by typing this command in your console:

```bash
npm test
```

## Contributing

PR is welcome!

**Notice:** You should make your changes only in `src` folder, don't try to edit files from `dist` as it compiled from `src` by babel and shouldn't be changes manually.
