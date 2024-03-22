<template>
  <div>
    <MainMenu :n1menu="menu"  />
  </div>
</template>

<script>
import MainMenu from './components/menu/MainMenu.vue'
import menujson from './api/data.json';

export default {
  name: 'App',
  components: {
    MainMenu
  },
  data() {
    return {
      screenWidthDesktop: window.innerWidth > 1200,
      screenWidthMob: window.innerWidth < 1200
    }
  },
  computed: {
    menu(){
      return menujson.menu;
    },
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
body {
  background: #fff;
  margin: 0;
}
</style>
