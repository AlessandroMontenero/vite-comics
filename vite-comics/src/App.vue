<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'


export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
 <AppHeader/>
 <AppMain />
 <AppFooter />
</template>

<style>
html, body {
  margin: 0;
  padding: 0;
  font-family: 'Raleway', sans-serif;
  
}
.container {
  width: 80%;
  margin: auto;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

li {
  padding: 0;
  margin: 0;
}

a {
  text-decoration: none;
  color: inherit;
}




</style>
