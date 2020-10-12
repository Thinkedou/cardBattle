<template>

  <div class="full_background">

      <BattleCard />
      <BattleCard char-img='https://cdn.dribbble.com/users/241205/screenshots/4614615/hacker-knight.png'/>

  </div>

</template>

<script >

import BattleCard       from './BattleCard.vue'

export default {
  name: 'BattleBackground',
  components:{
      BattleCard
  }

}
</script>


<style lang="scss">

html {
  background: url('https://images.wallpaperscraft.com/image/cliffs_waterfalls_sky_nature_trees_60068_1920x1080.jpg') no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}
.full_background{

    display:flex;
    justify-content: center;

}
</style>
