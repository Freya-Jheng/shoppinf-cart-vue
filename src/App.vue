<template>
  <div id="app">
    <Navbar />
    <div class="main">
      <router-view/>
    </div>
    <Footer />
  </div>
</template>
<script>
import Navbar from './components/Navbar.vue'
import Footer from './views/Footer.vue'
import 'bootstrap/dist/css/bootstrap.min.css'

export default {
  components: {
    Navbar,
    Footer,
  }
}


</script>




<style>
@import 'assets/scss/main.scss';

body {
  padding: 0;
  margin: 0;    
}
#app {
  text-align: center;
  border: 3px solid pink;
  width: 100%;
  color: #000000;
}
div, nav, h1, h2, h3, h4, h5, h6, p, img, input, section, label, a{
  text-align: center;
  padding: 0;
  margin: 0;
}
nav, a {
  text-decoration: none;
}

</style>
