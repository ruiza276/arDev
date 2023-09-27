<template>
<div>
  <Header />
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">arDev</h1>
      <div class="links">
        <a
          href="https://github.com/ruiza276"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
        <a
          href="https://www.linkedin.com/in/alex-r-6205b113b/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          Linkedin
        </a>
      </div>
    </div>
      <Footer />
  </div>
  </div>
</template>

<script>
export default {}
</script>


<style>
.container {
  margin: 0 auto;
  padding-bottom: 10px;
  justify-content: center;
  text-align: center;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

</style>
