<template>
  <Navbar/>
  <Data/>
  <Footer/>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: {
    Navbar,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

}

body{
  margin: 0;
  padding: 0;
}


nav {
  background-color: grey;
 
}

nav a {
  font-weight: bold;
  text-decoration: none;
  color: white;
}


</style>
