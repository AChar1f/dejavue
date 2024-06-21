<template>
  <div class="container">
    <Friends/>
  </div>

</template>

<script>
import Friends from './components/Friends.vue';

export default {
  name: 'App',
  components: {
     Friends
  },
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
