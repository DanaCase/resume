<template>
  <div class="hexagon">
    <div class="inner">
	<p class="text-center">Dana</p>
	<p class="text-center">Case</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'hexagon'
  }
</script>

<style scoped>
/*http://csshexagon.com/*/
.hexagon {
  position: relative;
  width: 225px; 
  height: 129.90px;
  margin: 64.95px 0;
  border-left: solid 5px #333333;
  border-right: solid 5px #333333;
}

.hexagon:before,
.hexagon:after {
  content: "";
  position: absolute;
  z-index: 1;
  width: 159.10px;
  height: 159.10px;
  -webkit-transform: scaleY(0.5774) rotate(-45deg);
  -ms-transform: scaleY(0.5774) rotate(-45deg);
  transform: scaleY(0.5774) rotate(-45deg);
  left: 27.9505px;
}

.hexagon:before {
  top: -79.5495px;
  border-top: solid 7.0711px #333333;
  border-right: solid 7.0711px #333333;
}

.hexagon:after {
  bottom: -79.5495px;
  border-bottom: solid 7.0711px #333333;
  border-left: solid 7.0711px #333333;
}/*.hexagon {*/
  /*position: relative;*/
  /*width: 300px; */
  /*height: 173.21px;*/
  /*background-color: $body-bg;*/
  /*margin: 86.60px 0;*/
  /*border-left: solid 5px #333333;*/
  /*border-right: solid 5px #333333;*/
/*}*/

/*.hexagon:before,*/
/*.hexagon:after {*/
  /*content: "";*/
  /*position: absolute;*/
  /*z-index: 1;*/
  /*width: 212.13px;*/
  /*height: 212.13px;*/
  /*-webkit-transform: scaleY(0.5774) rotate(-45deg);*/
  /*-ms-transform: scaleY(0.5774) rotate(-45deg);*/
  /*transform: scaleY(0.5774) rotate(-45deg);*/
  /*background-color: inherit;*/
  /*left: 38.9340px;*/
/*}*/

/*.hexagon:before {*/
  /*top: -106.0660px;*/
  /*border-top: solid 7.0711px #333333;*/
  /*border-right: solid 7.0711px #333333;*/
/*}*/

/*.hexagon:after {*/
  /*bottom: -106.0660px;*/
  /*border-bottom: solid 7.0711px #333333;*/
  /*border-left: solid 7.0711px #333333;*/
/*}*/
</style>
