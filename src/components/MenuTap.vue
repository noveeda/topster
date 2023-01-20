<template>
    <div class="container">
        <div class="titlebar">
            <div class="title">PopsteReview</div>
            <div class="logo"><img src="../assets/logo.png" width="40" height="40"/></div> 
        </div>
        
        <!-- 버튼 섹션 -->
        <div class="inline-flex">
            <MenuButton content="Download"/>
            <MenuButton content="Upload"/>
        </div>

        <div class="inline-flex">
            <MenuButton content="Back Up"/>
            <MenuButton content="Nickname"/>
        </div>

        <div class="inline-flex">
            <MenuButton content="Pstr/Cvr slct"/>
            <MenuButton content="Delete"/>
        </div>

        <!-- 검색바 섹션 -->
        <!-- TODO -->
        <!-- 검색바 안에 검색 버튼 넣기 -->
        <!-- 검색바 코너 라운드 넣기 -->
        <!-- 검색바 디자인 -->
        <div id="search-bar" class="search-bar">
            <!-- 검색 기능 만들어야함 -->
            <base-input :input="inputText" @update-input="updateInput"/>
        </div>
        
        <!-- 검색 결과 리스트 -->
        <div>

        </div>
    </div>
</template>

<script>
import MenuButton from './MenuButton.vue'
import BaseInput from './BaseInput.vue';

export default{
    name: 'MenuTap',
    components: {
        MenuButton,
        'base-input': BaseInput
    },
    data() {
        return{
            array: ['Download', 'Upload', 'Back Up', 'Nickname', 'Pstr/Cvr Slct', 'Delete'],
            inputText: ''
        }
    },
    methods: {
        updateInput(input){
            this.inputText = input
        },
        
    }
}

</script>

<style scoped>
.titlebar{
    margin-top: 0.5vh;
    margin-bottom: 0.5vh;
    height: 4vh;
    display: flex;
    justify-content: flex-end;
}
.logo{
    width: 100px;
    height: 0.01vh;
}
.logo > img{
    max-width: 100%;
}
.title{
    font-size: 3.5vh;
    font-weight: 700;
    font-family: 'Inter';
    color: #169A00;
}
.container{
    margin: 0;
    position: absolute;
    width: 18vw;
    height: 100vh;
    background: #404040;
    position: relative;
    display: flex;
    flex-direction: column;
    text-align: center;
}

.inline-flex{
    display: inline-flex;
    margin-bottom: 1vh;
    justify-content: space-evenly;
    font-size: 1vh;
}

.search-bar{
    height: 4vh;
    width: 100%;
    justify-content: center;
}

.search-bar > input{
    width: 92%;
    height: auto;
    line-height: 2.6vh;
    font-size: 2.6vh;
    border-color: #00C165;
    border-radius: 1vh;
    border-width: 0.4vh;
}
</style>