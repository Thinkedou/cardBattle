<template>
  <div id="app">
    <BattleBackground />
    <!-- <BattleCard /> -->
  </div>
</template>

<script>

// import BattleCard       from './components/BattleCard.vue'
import BattleBackground from './components/BattleBackground.vue'

export default {
  name: 'App',
  components: {
    // BattleCard,
    BattleBackground
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
