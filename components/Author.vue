<template>
  <div>
      <div class="container">
      <h4 class="sub-title">Author</h4>
      <p>{{ author.name }} - {{ author.bio }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      author: {
        type: Object,
        required: true
      }
    }
  }
</script>
<style scoped>

.container {
  margin: 0 auto;
  text-align: left;
  padding-bottom: 7.5%;
  font-family: system-ui;
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