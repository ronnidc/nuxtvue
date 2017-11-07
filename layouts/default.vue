<template>
  <div class="defaulttemplate">
    <section class="container">
      <div>
        <logo/>
        <article>
          <nuxt/>
        </article>
      </div>
    </section>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="scss">
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.button {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid transparent;
  text-decoration: none;
  padding: 10px 30px;
  transition: background-color .2s, color .2s;
  margin: 0 7.5px;
}

  .button--green {
    color: #3b8070;
    border-color: #3b8070;
  }

  .button--green:hover {
    color: #fff;
    background-color: #3b8070;
  }

  .button--grey {
    border-color: #35495e;
    color: #35495e;
  }

  .button--grey:hover {
    color: #fff;
    background-color: #35495e;
  }

.article-title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.article-subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.article-links {
  padding-top: 15px;
}
</style>
