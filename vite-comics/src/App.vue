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

<style lang="scss">
html, body {
  margin: 0;
  padding: 0;
  font-family: 'Raleway', sans-serif;
  
}

h2 {
  font-size: 1.2rem;
  margin: .8rem 0;
}

h3 {
  font-size: .9rem;
  margin: .6rem 0;
}

h4 {
  font-size: .8rem;
}

h5 {
  font-size: .8rem;
}

.blue {
  color: rgb(60, 130, 240);
}

.container {
  width: 80%;
  margin: auto;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  li {
    padding: 0;
    margin: 0;
  }
}


a {
  text-decoration: none;
  color: inherit;
}

a {
  opacity: .9;
  filter: brightness(100%);
  transition: all .1s linear;
}
a:hover {
  opacity: 1;
  filter: brightness(110%);
}




</style>
