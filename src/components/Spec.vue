<template>
    <BadashComponentStack class="Frontend"  :back="windowHeight">
        <p>FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END FRONT-END</p>
    </BadashComponentStack>
</template>
<script>
    import style from 'vue-styled-components'
    let back={
        back:Number
    }
    let BadashComponentStack = style('div',back)`
    overflow:hidden;
    height:${props => props.back}px;
    background-color: #f9d29d;
    background-image: linear-gradient(315deg, #f9d29d 0%, #ffd8cb 74%);
    p{
    @media screen and (min-width: 900px) {
    font-size:800px;
    }
    word-wrap: normal;
    display:flex;
    width:100%;
    margin:0;
    padding:0;
    font-family: 'Bebas Neue', cursive;
    font-size:350px;
    white-space:  nowrap ;
    }
  `
    export default {
        name:"Spec",
        components:{
            "BadashComponentStack":BadashComponentStack
        },
        data(){
            return{
                windowHeight:0
            }
        },
        created() {
            this.windowHeight = window.innerHeight
        }
    }
</script>
<style>

</style>