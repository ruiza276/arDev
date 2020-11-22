<template>
<section>
  <div class="Header">
    <div class="topnav">
      <a href="/">Home</a>
      <a href="about">About</a>
      <a href="#contact">Blog</a>
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
}
.topnav {
  background-color:rgb(23,	62	,67);
  overflow: hidden;
  position: relative;
  left: 0;
  top: 0;
  width: 100vw;
  padding-bottom: 10px;
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
  background-color: rgb(221,223,212);
  color: black;
}

</style>
