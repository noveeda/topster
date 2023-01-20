<template>
    <div class="button">
        <button type="button" v-on:click="btnClick">{{ content }}</button>
    </div>
</template>

<script>
export default{
    name : 'MenuButton',
    props: {
        content : String
    },
    methods:{
        btnClick: () =>{
            alert("asdasd");
        }
    }
}
</script>

<style scoped>
button{
    padding: 0;
    background: none;
    border: none;
    font-family: 'Inter';
    font-weight: 400;
    font-size: 2.5vh;
    color: white;
}
.button{
    width: calc(18vw/2);
    height: 4vh;
    margin: 0.5vh 0.5vw;
    border-radius: 1vh;
    box-shadow: 0vh 0.5vh 0.5vh rgba(0, 0, 0, 0.25);
    background-color: #646464;
}
</style>