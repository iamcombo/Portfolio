<template>
  <div class="px-24">
    <div class="grid grid-cols-2 gap-4 pt-24">
      <div class="text-6xl font-black leading-none">
        <p>Piset</p>
        <p>Heang.</p>
      </div>
      <div class="font-black text-white blur-bg">
        <p class="text-6xl font-black text-white">Introduction</p>
        <br>
        <p class="text-4xl">Web Design, Web Deverlopment with VUE.JS</p>
        <br>
        <p>Hi! My name is Piset Heang, and I'm a Cambodia-based freelancer.
          I'm working remotely on project for clients all over the world.
        </p>
        <hr>
        <p>I have diverse set of skills, ranging from design, to HTML CSS + Javascript, 
          all the way to VUE.JS & NUXT.JS
        </p>
        <br>
        <nuxt-link to="/" class="text-yellow-500">My Story >>></nuxt-link>
      </div>
    </div>
    <div class="story">
      
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.my_container {
  padding: 1% 6%;
}
.blur-bg {
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0, 0.6); /* Black w/opacity/see-through */
  padding: 1rem;
  border-radius: 6px;
}
</style>