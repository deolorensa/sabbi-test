<template>
  <v-app>
    <v-app-bar 
    color="rgb(0, 115, 255)"
    flat>
      <nav-bar/>
    </v-app-bar>
    <v-main style="background-image: linear-gradient(to bottom, rgb(0, 115, 255), white);">
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from './components/layout/NavBar.vue';
export default {
  name: 'App',
  components:{
    NavBar
  },
  data: () => ({
    //
  }),
}
</script>

<style>
.white{
  color: white;
}
.py{
  padding: 150px 0;
}

</style>
