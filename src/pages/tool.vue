<template>
  <page-container :h1-title="h1Title" :h2-title="h2Title" :page-content="pageContent"></page-container>
</template>
<script type="text/babel">
  import '../font/iconfont.css';
  import '../style/tool.css';
  export default {
    ready() {
      this.$http.get('/simulate/tool.json').then((data) => {
        this.$set('h1Title', data.body.h1Title);
        this.$set('h2Title', data.body.h2Title);
        this.$set('pageContent', data.body.pageContent);
      }, (data, status, request) => {
        console.log('fail' + status + ',' + request);
      });
    },
    data() {
      return {
        h1Title: '',
        h2Title: '',
        pageContent: ''
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
