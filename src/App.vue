<template>
  <div id="app">
    <div class="main">
      <MenuTap></MenuTap>
      <PosterList></PosterList>
      <PosterReview></PosterReview>
    </div>
  </div>
</template>

<script>
import MenuTap from './components/MenuTap.vue';
import PosterList from './components/PosterList.vue';
import PosterReview from './components/PosterReview.vue';

export default {
  name: 'App',
  components: {
    MenuTap, PosterList, PosterReview
  }
}
</script>

<style scoped>

.main{
  background-color: #202020;
  height: 100vh;
  width: 100vw;
  display: flex;
  position: absolute;
  top: 0px;
  left: 0px;
  margin: 0;
}
</style>