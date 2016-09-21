<template>
  <div class="nav">
    <header>
      <a href="/" class="nav-logo" alt="egg"><img src="../assets/images/xdc.png"></a>
      <ul>
        <li v-for="group in navs">
          <a v-for="item in group.list" v-link="{ path: item.path }" is-link>
            {{ item.name }}
        </a>
        </li>
      </ul>
    </header>
  </div>
</template>
<script type="text/babel">
  import '../style/demos.css';
  import '../font/iconfont.css';
  import { navs } from '../route';
  export default {
    data() {
      return {
        navs: []
      };
    },

    compiled() {
      this.navs = navs;
    }
  };
</script>
