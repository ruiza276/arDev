<template>
<section>
  <div class="Header">
    <div class="topnav">
    <NuxtLink to="/">Home</NuxtLink>
    <NuxtLink to="/about">About</NuxtLink>
    <NuxtLink to="/blog">Blog</NuxtLink>
    </div>
  </div>
</section>
</template>

<script>
export default {
    methods: {

    }
}
</script>

<style scoped>

/* Many Thanks to the folks are W3 */

.Header{
  display: inline-block;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding-bottom: 5%;
}
.topnav {
  background-color:rgb(23,	62	,67);
  overflow: hidden;
  position: fixed;
  left: 0;
  top: 0;
  width: 100vw;
  padding-bottom: 2%;
}

.topnav a {
  float: center;
  color: rgb(	63, 176, 172);
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 25px;
}

.topnav a:hover {
  background-color: #35495e;
  color: #fff;
}

</style>
