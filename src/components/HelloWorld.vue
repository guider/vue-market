<template>
  <div class="hello">
    <wheel-view></wheel-view>
  </div>
</template>

<script>

  import WheelView from "./wheel/Wheel.vue"
  import wheel from "./wheel/wheel.js"

  export default {
    components: {
      WheelView
    },
    name: 'HelloWorld',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    mounted() {
      let self = this
      this.wheel = new wheel(self, {
        areaNumber: 8,
        speed: 16,
        awardNumer: 1,
        mode: 1,
        callback: () => {
         console.log('success');
        }
      })
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
