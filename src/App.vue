<script>

import Block from './components/Block.vue'
export default{
  name:'App',
  components: { Block },
  data(){
    return{
      isPlaying: false,
      delay: null
    }
  },
  methods: {
    start(){
      this.delay = 2000 + Math.random()*5000
      this.isPlaying = true
      console.log(this.delay)
    }
  }
}
</script>

<template>
  <header>
  </header>

  
    <h1>Ninja Reaction Timer</h1>

    <button @click="start" :disabled="isPlaying">Play</button>
    <Block v-if="isPlaying" :delay="delay"/>


  
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
