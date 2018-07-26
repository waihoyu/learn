
<template>
  <div class = "main">
    <button v-on:click="show = !show">
      Toggle
    </button>
    <transition name="fade">
      <div v-if="show"  class="food">  
          111
      </div>
    </transition>
  </div>
</template>

<script>
　　export default {
    data () {
      return {
        show: true
      }
    }
  }
</script>

<style lang="stylus">
  .food 
      position fixed
      width 400px
      height 400px
      left 200px
      top 0
      bottom 48px
      z-index 30  
      background blue
      transition: all 1s linear
  .fade-enter, .fade-leave-to
    // animation: bounce-in .5s;
    background red
    transition: all 1s linear
    // transform: translate(-100%, 0, 0)
    transform: translate3d(100%, 0, 0)
  @keyframes bounce-in {
    from {
      background red
      }
    to {
        background yellow
        transform scaleX(0.1)
      }
  }
</style>