# Expanding

The Expanding Transition Component for Vue 2.0

## Installation

```
$ npm install vue-bulma-expanding --save
```

## Examples

```vue
<template>
  <router-link to="/charts" aria-expanded="show" @click.native="show = !show">
    <span class="icon is-small"><i class="fa fa-bar-chart-o"></i></span>
    Charts
    <span class="icon is-small is-angle"><i class="fa fa-angle-down"></i></span>
  </router-link>
  <expanding>
    <ul v-show="show">
      <li>
        <router-link to="/charts/chartjs">
          ChartJs
        </router-link>
      </li>
      <li>
        <router-link to="/charts/chartist">
          Chartist
        </router-link>
      </li>
      <li>
        <router-link to="/charts/peity">
          Peity
        </router-link>
      </li>
      <li>
        <router-link to="/charts/plotly">
          Plotly
        </router-link>
      </li>
    </ul>
  </expanding>
</template>

<script>
import Expanding from '../Expanding'

export default {
  components: {
    Expanding
  },

  data () {
    return {
      show: false
    }
  }
}
</script>
```

## Badges

![](https://img.shields.io/badge/license-MIT-blue.svg)
![](https://img.shields.io/badge/status-stable-green.svg)

---

> [fundon.me](https://fundon.me) &nbsp;&middot;&nbsp;
> GitHub [@fundon](https://github.com/fundon) &nbsp;&middot;&nbsp;
> Twitter [@_fundon](https://twitter.com/_fundon)

