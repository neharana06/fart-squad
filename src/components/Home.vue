<template>
  <div class="hello">
    <ion-button @click="clicked" v-if="!showContent">Click Me</ion-button>
    <div v-if="showContent"><h1 style="color:#c8d350;font-weight:bold;font-size:35px">Bazinga!</h1></div>
    <div class="center"  v-if="showImage">
        <ion-img src="https://mybasketblue.s3.ap-south-1.amazonaws.com/fartSquad.gif"></ion-img>
    </div>
    <audio loop id="audio" src="http://soundbible.com/mp3/Squish%20Fart-SoundBible.com-115133916.mp3"></audio>
    </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      showImage: false,
      showContent:false
    }
  },
  methods: {
    clicked () {
       this.showImage = true
       this.showContent = true
       var audio = document.getElementById("audio");
       setTimeout(function(){
         audio.play()
       }, 1100)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 350px;
}
</style>

