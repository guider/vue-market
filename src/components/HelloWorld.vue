<template>
  <div class="hello">
    <wheel-view ref="wheel"></wheel-view>
  </div>
</template>

<script>

  import WheelView from "./wheel/Wheel.vue"

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
