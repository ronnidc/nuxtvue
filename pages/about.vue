<template>
  <div>
   <h1 class="article-title animated bounce animation-config">
        About this
      </h1>
      <h2 class="article-subtitle">
        Terminal commands
      </h2>
      <h3>Development mode:</h3>
      <code>$ npm run dev</code>
      <h3>Build:</h3>
      <code>$ npm run build</code>
      <code>$ npm start</code>
      <div class="article-links">
        <a href="https://nuxtjs.org/" target="_blank" class="button button--lightgreen">Documentation</a>
        <a href="https://github.com/ronnidc/nuxtvue" target="_blank" class="button button--grey">GitHub</a>
        <a href="/" class="button button--green">Home</a>
      </div>
  </div>
</template>



<style lang="scss" scoped>

  code {
    display: block;
    text-align: left;
    padding-left: 10px;
    margin-bottom: 5px;
  }
  h2 {
    padding-bottom: 0;
  }
  h3 {
    text-align: left;
    margin-top: 15px;
    margin-bottom: 5px;
  }
  h1 {
    color: #3B8070 !important;
  }
  .animation-config {
    animation-delay: 3s;
    animation-iteration-count: 3;
  }

</style>
