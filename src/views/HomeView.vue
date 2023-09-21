<template>
  <div class="home">
    <div style="display: flex; align-items: center; margin-top: 5%; margin-left: 20%">
      <img src="../assets/me.jpeg">
      <div style="width: 40vw; margin-left: 60px">
        <h1 style="text-align: left; margin: 0px 0px 10px 0px">Brandon Chen</h1>
        <p style="text-align: left; font-weight: 550; margin-bottom: 5px;">About Me</p>
        <p style="text-align: left; margin-top: 0;">17 year old first year Bachelor of Computer Science Student, with a strong drive to excel in the field of technology</p>
      </div>
    </div>
    <!-- <div style="margin-top: 15%; border-top: solid 1px white;">

    </div> -->
  </div>
</template>

<style>
  /* img {
    width: 250px;
    height: 250px;
    border-radius: 50%;
    overflow: hidden;
  } */  

  @media only screen and (max-device-width: 400px) {
    h1 {
      width: 20vw;
      height: 20vw;
    }

    p {
      width: 30vw;
      height: 9vw;
    }
  }
  
  img {
    width: 20vw;
    height: 20vw;
    border-radius: 50%;
    overflow: hidden;
  }

</style>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    // HelloWorld
  }
}
</script>
