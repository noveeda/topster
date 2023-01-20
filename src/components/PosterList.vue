<template>
  <div class="container">
    <PosterItem v-for ="posterItem in 25" :key="posterItem"/>
  </div>
</template>


<script>
import PosterItem from './PosterItem.vue';

export default {
  name: 'PosterList' ,
  components: {
    PosterItem
  }
}

</script>

<style scoped>
.container{
  width: 90vh;
  height: 90vh;
  margin-top: 5vh;
  margin-left: 5vh;
  box-shadow: 1vh 1vh 0.25vh 0.125vh rgba(0, 0, 32, 0.443);
  
  background-color: black; 
  /* 2차원 레이아웃을 위한 grid */
  display: grid;
  /* cols rows를 전부 동일한 비율로 5x5 컷팅 */
  grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  /* 가로 정렬 */
  justify-items: center;
  /* 세로 정렬 */
  align-items: center;
}
</style>