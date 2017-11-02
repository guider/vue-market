<template>
  <div>
    <div class="wheel_wp">
      <div v-if="mode == 1">
        <img src="../../components/wheel/images/dial_bg.png"/>
        <!--style="-webkit-transform:rotate({{deg}}deg) translateZ(0);transform:rotate({{deg}}deg) translateZ(0)"-->

        <div class="wheel_pointer"
             @click="start">
          <img src="../../components/wheel/images/dial_pointer.png"/>
        </div>
      </div>
      <div v-if="mode == 2">
        <!--style="-webkit-transform:rotate({{deg}}deg) translateZ(0);transform:rotate({{ deg}}deg) translateZ(0)"-->
        <img src="../../components/wheel/images/dial_bg.png"
        />
        <div class="wheel_pointer" @click="start">
          <img src="../../components/wheel/images/dial_pointer.png"/>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        mode: 1
      }
    },
    methods: {
      start() {
        console.log('start in vue');
      }
    }
  }

</script>
<style scoped>

  .wheel_wp {
    width: 250px;
    height: 250px;
    position: relative;
    margin: 0 auto;
  }

  .wheel_wp image {
    display: block;
    width: 100%;
    height: 100%;
  }

  .wheel_wp .wheel_pointer {
    position: absolute;
    width: 75px;
    height: 75px;
    top: 50%;
    left: 50%;
    margin: -37.5px 0 0 -37.5px;
    transform-origin: 50% 50%;
  }

  .wheel_wp .wheel_pointer image {
    position: absolute;
    width: 75px;
    height: 119px;
    left: 0;
    top: -32px;
  }

</style>
