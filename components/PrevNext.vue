<template>
<div class="container">
  <div class="prevnexlinks">
    <NuxtLink
      v-if="prev"
      :to="{ name: 'blog-slug', params: { slug: prev.slug } }"
      class="button--grey"
    >
      {{ prev.title }}
    </NuxtLink>
    <span v-if="next && prev">
    &nbsp;
    &nbsp;
    &nbsp;
    </span>
    <NuxtLink
      v-if="next"
      :to="{ name: 'blog-slug', params: { slug: next.slug } }"
      class="button--grey"
    >
      {{ next.title }}
    </NuxtLink>
  </div>
</div>
</template>

<script>
  export default {
    props: {
      prev: {
        type: Object,
        default: () => null
      },
      next: {
        type: Object,
        default: () => null
      }
    }
  }
</script>
<style>

.container {
  margin: 0 auto;
  justify-content: center;
  text-align: center;
  font-family: system-ui;
}

.prevnexlinks {
  padding-bottom: 3%;
}

.prevnexlinks a{
  color: #35495e;
  text-decoration: none;
}


.prevnexlinks a:hover {
  color: #fff;
  text-decoration: none;
  background-color: #35495e;
}
</style>
