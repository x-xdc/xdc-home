<template>
    <iframe src="http://ant.design/docs/pattern/navigation" frameborder="0" width="100%" height="800px"></iframe>
</template>

<script type="text/babel">
  import '../font/iconfont.css';

  export default {
    data() {
      return {
        smallScreen: true,
        isMobile: false,
        logoAnimateReady: false,
        descAnimateReady: false
      };
    },

    methods: {
      handleResize() {
        this.smallScreen = document.body.clientWidth <= 650;
      }
    },

    compiled() {
      this.logoAnimateReady = true;
      setTimeout(() => {
        this.descAnimateReady = true;
      }, 500);
      this.handleResize();
      window.addEventListener('resize', () => {
        this.handleResize();
      });
      this.isMobile = document.body.clientWidth <= 500;
    },

    beforeDestroy() {
      window.removeEventListener('resize', () => {
        this.handleResize();
      });
    }
  };
</script>
