<template>
  <!--<div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>-->
  <div id="app">
      <div :class="rotate? 'circle':'circle_chg'" @click="start"></div>
  </div>
  <!--<div>-->
    <!--<canvas id="myCanvas" width="300" height="150" style="border:1px solid #d3d3d3;">-->
      <!--Your browser does not support the HTML5 canvas tag.-->
    <!--</canvas>-->
  <!--</div>-->
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      rotate: false
    }
  },
  methods: {
    start () {
      this.rotate = !this.rotate
      console.log(this.rotate)
    }
  }
  // mounted () {
  //   var c = document.getElementById('myCanvas')
  //   var ctx = c.getContext('2d')
  //   ctx.beginPath()
  //   ctx.arc(100, 75, 50, 0, 2 * Math.PI)
  //   ctx.stroke()
  // }
}
</script>

<style>
/*#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
  .circle {
    width: 350px;
    height: 350px;
    border-radius: 175px;
    top: 100px;
    left:-175px;
    margin-left:50%;
    background-color:red;
    position:absolute;
    animation:changDeg 2s linear 0.2s infinite;
  }
  .circle_chg {
    width: 350px;
    height: 350px;
    border-radius: 175px;
    top: 100px;
    left:-175px;
    margin-left:50%;
    background-color:yellow;
    position:absolute;
    animation:changDeg 2s linear 0.2s infinite;
  }
  //定义动画
  @keyframes change changeDeg{
    0% {
      transform: rotate(0deg)
    }
   100% {
     transform:rotate(60deg)
   }
                    }
</style>
