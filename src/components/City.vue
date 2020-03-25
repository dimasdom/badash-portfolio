<template>
    <BadashComponentCity :back="windowHeight">
        <h1 class="display-2 text-center">CAN WORK IN</h1>
        <div  class="carousel slide" data-ride="carousel" data-interval="1800">
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <p>KYIV</p>
                </div>
                <div class="carousel-item">
                    <p>KHARKOV</p>
                </div>
                <div class="carousel-item">
                    <p>ODESSA</p>
                </div>
                <div class="carousel-item">
                    <p>DNIPRO</p>
                </div>
                <div class="carousel-item">
                    <p>LVIV</p>
                </div>
                <div class="carousel-item">
                    <p>VINNYTSIA</p>
                </div>
                <div class="carousel-item">
                    <p>I.FRANKIVSK</p>
                </div>
            </div>
        </div>
    </BadashComponentCity>

</template>

<script>
    import style from 'vue-styled-components'
    let back={
        back:Number
    }
    let BadashComponentCity = style('div',back)`
  height:${props => props.back}px;
    .display-2{
  font-size:50px;
  @media screen and (min-width: 900px) {
  font-size:100px;

  }
  }
  p{
  @media screen and (min-width: 900px) {
  font-size:300px;
  padding-top:7%;
  }
  margin:0;
  padding:0;
  padding-top:70%;
  text-align: center;
  font-size:60px;
  color:rgba(255,255,255,.1);
  background:url("https://media.giphy.com/media/l3fQ9icfExRfiePrq/giphy.gif");
  -webkit-background-clip: text;
}

  `
    export default {
        name: 'City',
        props: {
            msg: String
        },
        components:{
            "BadashComponentCity":BadashComponentCity ,
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
