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
    animation-delay: 4s;
    animation-iteration-count: 2;
  }

</style>
