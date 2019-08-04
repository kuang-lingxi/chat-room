<template>
  <div id="app">
    <span>hello</span>
    <Sidebar></Sidebar>
  </div>
</template>

<script>
import Sidebar from './components/ChatRoom/Sidebar';

export default {
  name: 'App',
  components: {
    Sidebar
  }
}
</script>

<style scoped>
/* * {margin:0;padding:0} */
#app {

}
</style>
