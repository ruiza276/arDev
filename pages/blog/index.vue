<template>
  <div class="container">
  <Header />
    <h1 class="Blog-title">Blog Posts ✍️</h1>
    <ul>
      <li v-for="article of articles" :key="article.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }"
        class="blog-links"
        >
          <img :src="article.img" />
          <div>
            <h2 class="blog-sub-title">{{ article.title }}</h2>
            <p>by {{ article.author.name }}</p>
            <p>{{ article.description }}</p>
          </div>
        </NuxtLink>
      </li>
    </ul>
    <Footer />
  </div>
</template>
<script>
import LayoutDefault from '../../layouts/default.vue';

  export default {
    components : {
        LayoutDefault
    },
    async asyncData({ $content, params }) {
      const articles = await $content('articles', params.slug)
        .only(['title', 'description', 'slug', 'author'])
        .sortBy('createdAt', 'desc')
        .fetch()

      //console.log(articles);

      return {
        articles
      }
    }
  }
</script>

<style scoped>
.container {
  margin: 0 auto;
  text-align: left;
  padding-top: 25px;
  padding-bottom: 55px;

}

.blog-links {
  color: #35495e;
  text-decoration: none;
  font-size: 15px;
  display: inline-block;
}

ul {
  list-style-type: none;
}

.Blog-title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: inline-block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
}

.blog-sub-title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-weight: 700;
  font-size: 25px;
  color: #35495e;
}

.blog-sub-title:hover {
  color: #fff;
  background-color: #35495e;
  overflow: hidden;
}

</style>