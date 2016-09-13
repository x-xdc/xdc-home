<template>
<div class="nav">
  <header>
    <a href="/" class="nav-logo" alt="egg"><img src="./assets/images/xdc.png"></a>
    <ul>
      <li v-for="group in navs">
        <a
          v-for="item in group.list"
          v-link="{ path: item.path }"
          is-link>
            {{ item.name }}
        </a>
      </li>
    </ul>
  </header>
</div>
<div class="index">
  <div class="banner block index-bg-dark">
    <div class="banner-logo" id="logo" style="position: relative;"><img src="./assets/images/logo.png" width="640" height="500" style="width: 320px; height: 250px;"></div>
    <h1>Born to build better enterprise frameworks and apps</h1>
    <p class="banner-button">
      <a class="btn btn-primary" href="/guide/">Get Started</a>
    </p>
  </div>
<!--
  <div class="version">
    <span>Latest: <strong>0.2.0</strong></span>
    <span>Node.js &gt;= <strong> 4.0.0</strong></span>
  </div> -->

  <div class="info index-bg-light">
    <ul>
      <li class="info-bg-grey">
        <div class="info-img">
          <img src="./assets/images/design.png">
        </div>
        <div class="info-write ">
          <h3>Powerful Plugin System</h3>
          <p>Do what you like in egg with the pluggable and extendable system</p>
        </div>
      </li>
      <li>
        <div class="info-img">
          <img src="./assets/images/fed.png">
        </div>
        <div class="info-write">
          <h3>Powerful Plugin System</h3>
          <p>Do what you like in egg with the pluggable and extendable system</p>
        </div>
      </li>
      <li class="info-bg-grey">
        <div class="info-img">
          <img src="./assets/images/operate.png">
        </div>
        <div class="info-write">
          <h3>Powerful Plugin System</h3>
          <p>Do what you like in egg with the pluggable and extendable system</p>
        </div>
      </li>
      <li>
        <div class="info-img">
          <img src="./assets/images/pro.png">
        </div>
        <div class="info-write">
          <h3>Powerful Plugin System</h3>
          <p>Do what you like in egg with the pluggable and extendable system</p>
        </div>
      </li>
    </ul>
  </div>

  <div class="guide block">
    <h2 class="ft-b">Get Started</h2>
    <div class="guide-code">
      <ul>
        <li><strong>$</strong>npm install xdc-cli -g</li>
        <li><strong>$</strong>xdc create my-vue-project vue</li>
        <li><strong>$</strong>cd my-vue-project</li>
        <li><strong>$</strong>xdc watch</li>
        <li><strong>$</strong>xdc dist -p</li>
      </ul>
    </div>
    <p>
      <a class="btn btn-primary" href="/guide/">Read More</a>
    </p>
  </div>
</div>
<div class="footer">
  <footer>
    <ul><li><a href="/guide/" alt="Guide">Guide</a></li><li><a href="https://xdc.party/" alt="Plugins">Plugins</a></li><li><a href="/release/" alt="Release">Release</a></li></ul>
    <div class="license">Released under the MIT License </div>
  </footer>
</div>
</template>

<style>
@import "./style/demos.css";

</style>

<script type="text/babel">
  import { navs } from './route';

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
