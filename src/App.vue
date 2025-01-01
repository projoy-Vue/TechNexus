<template>
  <div id="app">
    <NavBar />
    <router-view />
    <Footer/>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    NavBar,
    Footer,
  },
};
</script>

<style>
/* Optional global styles */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
