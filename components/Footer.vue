<template>
<div class="container">
<div class="footer-container">
  <h3>arDev</h3>
</div>
</div>
</template>

<script>
export default {
    props: ['foot']
}
</script>

<style scoped>
.footer-container {
  background-color:rgb(23,	62	,67);
  overflow: hidden;
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100vw;
  display: inline-block;
  font-family: system-ui;
}

.footer-container h3 {
  color: rgb(	63, 176, 172);;
  text-align: left;
  float: left;
  padding-left: 10px;
}
</style>
