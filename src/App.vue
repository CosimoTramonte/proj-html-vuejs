
<script>
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import MoreAbout from './components/MoreAbout.vue';
import AudioBook from './components/AudioBook.vue';


export default {
  name:"App",
  components:{
    Header,
    Jumbotron,
    MoreAbout,
    AudioBook
  }
}
</script>

<template>

  <div class="background">
    <div class="wrapper">
      <Header/>
      <Jumbotron/>
    </div>

    <MoreAbout/>
    <AudioBook/>
  </div>

</template>

<style lang="scss">
  @use "./scss/main.scss";

  .background{
    width: 100vw;
    height: 100vh;
    background-image: url("./assets/img/hero-07-2x.jpg");
    background-repeat: no-repeat;
    background-size: cover; 
    background-position: center;

    .wrapper{
      width: 100%;
      height: 100%;
      background: linear-gradient( rgba(0, 0, 0, 0.3),  rgba(0, 0, 0, 0.7));
    }
  }
</style>