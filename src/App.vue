<template>
  <div class="z-n1 position-absolute bg">
    <SideBar></SideBar>
    <Button></Button>
  </div>
  
</template>

<script>
import Button from './components/BootstrapButton.vue'
import SideBar from './components/SideBar.vue'

export default {
  name: 'App',
  components: {
    SideBar,
    Button
  }
}
</script>

<style scoped>
.bg {
  float: right;
  width: 100vw;
  height: 100vh;
  background: linear-gradient(155deg,#3E52BE66,#9031BDB3, #C72F2FFF);
}
</style>

