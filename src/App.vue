<template>
  <div class = "main">
    <button v-on:click="show = !show">
      Toggle
    </button>
    <transition name="fade">
      <p v-if="show">hello</p>
      <div  class="food">  
          111
      </div>
    </transition>
  </div>
</template>

<script>
　　export default{
    data() {
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
      transform all 0.3s linear

  .fade-transition
    transition: all 0.2s linear
    transform: translate3d(0, 0, 0)
  .fade-enter, .fade-leave-to
    animation: bounce-in .5s;
    transition: all 0.2s linear
    transform: translate3d(100%, 0, 0)
    background yellow 
  @keyframes bounce-in {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(1);
    }
  }
</style>
