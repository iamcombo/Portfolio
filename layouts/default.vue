<template>
  <div>
    <Sidebar />
    <Nuxt />
  </div>
</template>

<script>
import Sidebar from '~/components/Sidebar.vue';
export default {
  components: {
    Sidebar
  }
}
</script>

<style>
html {
  font-family:
    'Raleway'
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  background: url('../assets/hero-img.jpeg') no-repeat 50% 50%;
  background-size: cover;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
.pro_container {
  padding: 0 6%;
  height: auto;
}
</style>
