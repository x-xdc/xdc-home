<template>
  <div id="container">
    <navigation></navigation>
    <div class="page-title center">
      <h1>{{ h1Title }}</h1>
      <h2>{{ h2Title }}</h2>
    </div>
    <div class="page-main">
      <div class="markdown-body">
        {{{pageContent}}}
      </div>
    </div>
    <div class="ui-iframe">
      {{{uiIframe}}}
    </div>
    <div class="footer">
      <footer>
        <ul>
          <li><a href="/guide/" alt="Guide">Guide</a></li>
          <li><a href="https://xdc.party/" alt="Plugins">Plugins</a></li>
          <li><a href="/release/" alt="Release">Release</a></li>
        </ul>
        <div class="license">Released under the MIT License </div>
      </footer>
    </div>
  </div>
</template>
<script type="text/babel">
  export default {
    props: ['h1Title', 'h2Title', 'pageContent', 'uiIframe']
  };
</script>
