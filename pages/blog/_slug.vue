<template>
  <article>
  <Header />
  <div class="container">
    <h1 class="titleBlog">{{ article.title }}</h1>
    <p class="sub-title">{{ article.description }}</p>
    <p>{{ article.content }} </p>
</div>
    <!-- <nav>
  <ul>
    <li v-for="link of article.toc" :key="link.id">
      <NuxtLink :to="`#${link.id}`">{{ link.text }}</NuxtLink>
    </li>
  </ul>
</nav> -->
    <nuxt-content :document="article" />
    <author :author="article.author" />
    <prev-next :prev="prev" :next="next" />
      <Footer />
  </article>
</template>

<script>
  export default {
async asyncData({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    const [prev, next] = await $content('articles')
      .only(['title', 'slug'])
      .sortBy('createdAt', 'asc')
      .surround(params.slug)
      .fetch()

    return {
      article,
      prev,
      next
    }
  },
    methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
 }
  }
</script>
<style scoped>

.container {
  margin: 0 auto;
  text-align: left;
  padding-bottom: 5%;
  font-family: system-ui;
}
.links {
  color: #35495e;
  text-decoration: none;
}

.links:hover {
  color: #fff;
  background-color: #35495e;
}
.titleBlog {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 900;
  font-size: 200%;
  color: #35495e;
  letter-spacing: 1px;
  padding-top: 3%;
}

.sub-title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 25px;
  color: #35495e;
}

</style>