<template>
  <div>
    <header>Workshop : "To do List with Vue.js</header>
    <div class="imageHeader"><img src=".././assets/logo_vue.png" /></div>
  </div>
</template>

<script>
export default {
  props: ["listElement"],
  name: "HeaderList",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  background-color: #34495e;
  width: 100%;
  min-height: 5rem;
  text-align: center;
  line-height: 5rem;
  font-size: 1.5rem;
  color: white;
}
img {
  position: absolute;
  top: 0px;
}
</style>