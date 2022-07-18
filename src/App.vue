<script setup>
import HeadComp from "./components/template/HeaderComp.vue";
</script>
<template>
  <HeadComp />
  <main>
    <RouterView />
  </main>

  <footer id="footer">footer</footer>
</template>

<style>
@import "@/assets/base.css";
@import "@/assets/style.css";

#app {
  font-size: 16px;
  height: 100vh;
  width: 100vw;

  font-weight: normal;
}

header,
footer {
  background-color: rgb(213, 21, 21);
  color: white;
  height: 15%;
  font-size: 1.3rem;
  display: flex;
  align-items: center;
  padding-left: 2rem;
  
}
main {
  height: 70%;
}
</style>
