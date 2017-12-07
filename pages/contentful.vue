<template>
  <div>
   <h1 class="article-title animated bounce animation-config">
		<!-- render data of the person -->
			{{ person.fields.name }}
		</h1>
		<!-- render blog posts -->
		<ul class="blog-list">
			<li v-for="post in posts" :key="post.id">
			<strong>{{ post.fields.title }}</strong><br />
			{{ post.fields.description }}
			</li>
		</ul>
      <div class="article-links">
        <a href="https://nuxtjs.org/" target="_blank" class="button button--lightgreen">Documentation</a>
        <a href="https://github.com/ronnidc/nuxtvue" target="_blank" class="button button--grey">GitHub</a>
        <a href="/" class="button button--green">Home</a>
      </div>
  </div>
</template>

<script>
  import {createClient} from '~/plugins/contentful.js'

  const client = createClient()

  export default {
    // `env` is available in the context object
    asyncData ({env}) {
      return Promise.all([
        // fetch the owner of the blog
        client.getEntries({
          'sys.id': env.CTF_PERSON_ID
        }),
        // fetch all blog posts sorted by creation date
        client.getEntries({
          'content_type': env.CTF_BLOG_POST_TYPE_ID,
          order: '-sys.createdAt'
        })
      ]).then(([entries, posts]) => {
        // return data that should be available
        // in the template
        return {
          person: entries.items[0],
          posts: posts.items
        }
      }).catch(console.error)
    }
  }
</script>



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

  .blog-list {
	  list-style: none;
	  margin: 0;

	  li {
		  margin-bottom: 12px;

	  }
  }

</style>
