<template>
    <BadashComponentMain :back="windowHeight">
        <div id="myCarousel" class="carousel" data-ride="carousel" data-interval="400">
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <p>DO</p>
                    <span></span>
                </div>
                <div class="carousel-item">
                    <p>ДЕЛАЙ</p>
                    <span></span>
                </div>
                <div class="carousel-item">
                    <p>РОБИ</p>
                    <span></span>
                </div>
                <div class="carousel-item">
                    <p>FAIRE</p>
                    <span></span>
                </div>
                <div class="carousel-item">
                    <p>TUN</p>
                    <span></span>
                </div>
                <div class="carousel-item">
                    <p>FARE</p>
                    <span></span>
                </div>
                <div class="carousel-item">
                    <p>動</p>
                    <span></span>
                </div>
            </div>
        </div>
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
    padding-top:8%;
    }
    margin:0;
    padding:0;
    padding-top:70%;
    text-align: center;
    font-size:90px;
    color:white;

}

  `
    export default {
        name: 'Do',
        props: {
            msg: String
        },
        components:{
            "BadashComponentMain":BadashComponentMain ,
        },
        data(){
            return{
                windowHeight:0,
            }
        },
        created() {
            this.windowHeight = window.innerHeight
        },
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->


<style scoped>
    .carousel-item{
        height: 100vh;
        min-height:300px;
        background-image:url("https://wallpaperaccess.com/full/1374050.jpg");
        backface-visibility: visible;
        background-size:cover;
        background-repeat: no-repeat;
        background-position: center;

    }
</style>
