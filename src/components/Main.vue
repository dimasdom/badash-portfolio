<template>
 <BadashComponentMain :back="windowHeight">
  <div class="loadcircle"></div>
  <p>BADASH</p>
 </BadashComponentMain>
</template>

<script>
  import style from 'vue-styled-components'
  let back={
    back:Number
  }
  let BadashComponentMain = style('div',back)`
  height:${props => props.back}px;
  p{
  @media screen and (min-width: 900px) {
  font-size:300px;
  padding-top:7%;
  }
  margin:0;
  padding:0;
  padding-top:70%;
  text-align: center;
  font-size:70px;
  color:rgba(255,255,255,.1);
  background:url("https://media0.giphy.com/media/8UGoPsk9dSkkcQrzT0/giphy.gif");
  -webkit-background-clip: text;
}

  `
export default {
  name: 'Main',
  props: {
    msg: String
  },
  components:{
    "BadashComponentMain":BadashComponentMain ,
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
