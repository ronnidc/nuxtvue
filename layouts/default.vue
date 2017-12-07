<template>
  <div class="defaulttemplate">
    <section class="container">
      <div>
        <logo/>
        <article>
          <nuxt/>
          
        </article>
        <div class="article-links">
          <a href="https://nuxtjs.org/" target="_blank" class="button button--grey">Documentation</a>
          <a href="https://github.com/ronnidc/nuxtvue" target="_blank" class="button button--grey">GitHub</a>
          <a href="/" class="button button--green">Home</a>
          <a href="/about" class="button button--green">About</a>
          <a href="/contentful" class="button button--lightgreen">Contentful</a>
        </div>
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


