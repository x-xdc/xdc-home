<template>
  <page-container :h1-title="h1Title" :h2-title="h2Title" :page-content="pageContent" :ui-iframe="uiIframe"></page-container>
</template>
<script type="text/babel">
  import '../font/iconfont.css';

  export default {
    ready() {
      this.$http.get('/simulate/components.json').then((data) => {
        this.$set('h1Title', data.body.h1Title);
        this.$set('h2Title', data.body.h2Title);
        this.$set('pageContent', data.body.pageContent);
        this.$set('uiIframe', data.body.uiIframe);
      }, (data, status, request) => {
        console.log('fail' + status + ',' + request);
      });
    },
    data() {
      return {
        h1Title: '',
        h2Title: '',
        pageContent: '',
        uiIframe: ''
      };
    },

    methods: {
    },
    compiled() {
    },
    beforeDestroy() {
    }
  };
</script>
