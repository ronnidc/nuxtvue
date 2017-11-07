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


