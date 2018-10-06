<template>
  <!--<div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>-->
  <div id="app">
    <img src="./assets/rotate.jpeg" class="rotateImg"/>
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
  methods: {
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
*{
  margin: 0;
  padding: 0;
}
.rotateImg {
  width: 400px;
  animation:circleRoate 10s ;
  animation-timing-function:linear;
}
@keyframes circleRoate{
  from{transform: rotate(0deg) infinite;}
  to{transform: rotate(360deg);}
}

</style>
