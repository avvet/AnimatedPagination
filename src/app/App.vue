<template>
  <div>
    <router-view></router-view>

    <!--<image-container></image-container>-->
    <!--<animated-list></animated-list>-->
  </div>
</template>

<script>
  import AnimatedList from "Components/animated-list-component/AnimatedList";

  export default {
    data() {
      return {

      }
    },
    name: 'App',
    components: {
      animatedList: 'AnimatedList'
    }
  }

</script>


<style>
  #app {
    /*font-family: 'Open Sans', Helvetica, Arial, sans-serif;*/
    font-family: 'Montserrat', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }


</style>