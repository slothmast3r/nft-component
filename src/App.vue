<template>
  <div class="app">
    <div class="card">
      <div class="card-wrapper">
        <div class="card-top">
          <div style="position: relative">
      <img class="image etherum" :src="require('/src/assets/images/image-equilibrium.jpg')">

          <div class="overlay">
            <img :src="require('/src/assets/images/icon-view.svg')">
          </div>
          </div>
      <div class="card-title">
      Equilibrium #3429
      </div>
        <div class="card-subtitle">
      Our Equilibrium collection promotes balance and calm.
        </div>
        <div class="card-row">
        <div class="card-amount">
      <img :src="require('/src/assets/images/icon-ethereum.svg')"><div>0.041 ETH</div> </div>
        <div class="card-time">
      <img :src="require('/src/assets/images/icon-clock.svg')"> <div>3 days left</div></div>
        </div>
        </div><div class="card-bottom">
        <img class="avatar" :src="require('/src/assets/images/image-avatar.png')"> <div> Creation of <span class="owner-name"> Jules Wyvern </span> </div>

      </div>

      </div>

    </div>
    <div class="attribution">
      Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
      Coded by <a href="https://github.com/slothmast3r">slothmast3r</a>.
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style lang="scss">
@import url("https://fonts.google.com/specimen/Outfit");
$soft_blue: hsl(215, 51%, 70%);
$cyan: hsl(178, 100%, 50%);
$dark_blue_bg: hsl(217, 54%, 11%);
$dark_blue_card: hsl(216, 50%, 16%);
.app {
  font-family: Outfit, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-size: 18px;
  align-items: center;

  font-weight: 300;
  color: $soft_blue;
}
body{
  margin: 0;
  background: $dark_blue_bg;
}

.card{
  margin:100px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 400px;
  background: $dark_blue_card;
  border-radius: 10px;
  box-shadow: 10px 10px 10px #0c1729;
  @media only screen and (max-width: 375px)  {
    width: 300px;
    .card-title{
      font-size: 18px;
    }
    font-size: 16px;
  }
  .card-top{
    margin-bottom: 20px;
    padding-bottom: 20px;
    border-bottom: 1px solid $soft_blue;
  }
  .card-wrapper{
    padding: 20px;
  }
.etherum{
  width: 360px;
  border-radius: 10px;
  @media only screen and (max-width: 375px)  {
    width: 260px;
  }
}
  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 255, 247, 0.4);
    width: 100%;
    height: calc(100% - 5px);
    opacity: 0;
    transition: all 300ms ease-out;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 10px;
    img{
      width: 100px;
      height: 100px;
    }
  }

  .overlay:hover,
  .overlay:active {
    opacity: 1;
    cursor: pointer;
  }
  .card-title{
    color: white;
    margin: 20px 0;
    font-weight: 600;
    font-size: 20px;
    transition: all 300ms ease-out;
  }

  .card-title:active,
  .card-title:hover{
    color: $cyan;
    cursor: pointer;
  }
  .card-subtitle{
    margin: 20px 0;
    font-weight: 300;
  }
  .card-row{
    img{
      margin-right: 5px;
    }
    display: flex;
    justify-content: center;
    .card-amount{
      display: flex;
      align-items: center;
      flex-grow: 1;
      color: $cyan;
    }
.card-time{
  display: flex;
  flex-grow: 1;
  text-align: right;
  justify-content: right;
  align-items: center;
}
  }
  .card-bottom{
  .avatar{
    border: 1px solid white;
    border-radius: 30px;
    width: 30px;
    height: 30px;
    margin-right: 10px  ;

  }
  .owner-name{
    color: white;
  }
    display: flex;
    align-items: center;
  }
}
</style>
