<template>

  <div class="mainCard">
    <div class="ft-recipe__thumb">
     <img :src="charImg" />
    </div>
    <div class="ft-recipe__content">

      <header class="content__header">

        <div class="row-wrapper">
          <h2 class="recipe-title">Wandering elve</h2>
          <div class="user-rating"></div>
        </div>

      </header>
      <div class="content_display">
          <div class="content__life">
              <span class='lifeLevel'>82/100</span><progress class='life_progress' max="100" value="80"></progress>
          </div>

          <div class="footer__action">
              <button type="button" class='btn btn_attack' @click='handleAttackBtn'></button>
              <button type="button" class='btn btn_heal'></button>
          </div>
      </div>


    </div>
  </div>

</template>

<script >
export default {
  name: 'BattleCard',
  props:{
    charImg:{
        type:String,
        default:'https://cdn.dribbble.com/users/1742746/screenshots/13487846/media/64161929038ef47e8352e13478d162b1.png'
    }
  },
  methods:{
      handleAttackBtn:()=>{
          console.log('attaque deLVES!!');
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" >
@import url('https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Work+Sans:wght@300;400;500;600;700&display=swap');

:root {
    --headlinesFont: 'Jost', sans-serif;
    --bodyFont: 'Work Sans', sans-serif;
    --fuelYellow: #f0a035;
    --textColor: #323232;
    --bodyBg: #d6d6d6;
    --white: #fff;
    --black: #000;
}

@mixin poCentering {

}

body {

    font-family: var(--bodyFont);
    color: var(--textColor);
    line-height: 1.5;
}

* {
    -webkit-box-sizing: inherit;
    -moz-box-sizing: inherit;
    box-sizing: inherit;
}

img {
    vertical-align: text-bottom;
}

a {
    color: inherit;
    text-decoration: none;
}


.mainCard {
    width: 360px;
    height: 560px;
    background: var(--white);
    display: flex;
    margin-left:20px;
    border-radius:5px;
    flex-direction: column;
    box-shadow: 0 0 88px 0 rgba(0, 0, 0, 0.1607843137254902);
    overflow: hidden;
    @include poCentering;
    .ft-recipe__thumb {
        position: relative;
        height: 281px;
        box-shadow: 0px 0px 130px 0 rgba(0, 0, 0, 0.38);

        h3 {
            text-align: center;
            position: absolute;
            margin: 0;
            width: 100%;
            color: var(--white);
            font-family: var(--headlinesFont);
            font-size: 25px;
            height: 100%;
            background: linear-gradient(to bottom, rgba(0, 0, 0, 0.25), transparent);
            padding: 2.4rem 0 0;
        }
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: 50% 50%;
        }
    }
    .ft-recipe__content {
        flex: 1;

        padding: 0 2em 1em;
        .content__header {
            .row-wrapper {
                display: flex;
                padding: .55em 0 .3em;
                border-bottom: 1px solid #d8d8d8;
                .recipe-title {
                    font-family: var(--headlinesFont);
                    font-weight: 600;
                }

            }

        }

    }

    .content_display{
        margin-top:50px;

        .life_progress{
            margin-left: 10px;
            width: 200px;
            height:10px;
            background-color: #eee;
            border-radius: 4px;

        }
        .life_progress::-webkit-progress-value{
            background-color: red;
            border-radius: 4px;
        }
        .life_progress::-webkit-progress-bar{
            background: black;
            border-radius: 4px;
        }
        .lifeLevel{
            font-family: var(--headlinesFont);
            font-weight: 600;
        }
        .footer__action {
            display:flex;
            height:100px;
            align-items: flex-end;
            .btn{
                display: block;
                border:0;

                padding: 0;
                height:  45px;
            }
            .btn_attack {
                width:  145px;
                background-image: url('/img/btn_attack.png');
            }
            .btn_heal {
                width:  140px;
                background-image: url('/img/btn_heal.png');

            }
        }
    }

}


</style>
