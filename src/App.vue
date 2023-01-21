<template>
  <div id="app">
    <div class="main">
      <MenuTap>
        <MenuButton v-for="button in buttons" :key="button" v-bind:name="button"></MenuButton>
      </MenuTap> 
      <PosterList></PosterList> 
      <PosterReview></PosterReview>  
    </div>
  </div>
</template>

<script>
import MenuButton from './components/MenuButton.vue';
import MenuTap from './components/MenuTap.vue';
import PosterList from './components/PosterList.vue';
import PosterReview from './components/PosterReview.vue';

const HOST    = 'https://ws.audioscrobbler.com/2.0/?'

export default {
  name: 'App',
  data(){
    return{
      result: '',
      buttons: [
        'Download', 
        'Upload', 
        'Back Up', 
        'NickName', 
        'Pstr/Cvr Slct', 
        'Delete'
      ]
    }
  },
  components: {
    MenuTap, MenuButton, PosterList, PosterReview
  },
  methods:{
    loadApiData(){
      this.$axios
        .get(HOST, {
          params: {
            method      : 'album.search',
            album       : 'aimer',
            api_key     : process.env.VUE_APP_LASTFM_API_KEY,
            format : 'json'
          }
        }).then((res) => {
          console.log(res.data)
          this.result = res.data['results']['albummatches']['album'][0]['image'][3]['#text']
        }).catch((error) => {
          console.error(error)
        }).finally(() => {
          console.log('API 호출 끝')
        })
    }
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
  margin: 0;
}
</style>