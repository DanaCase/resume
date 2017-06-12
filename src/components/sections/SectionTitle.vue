<template>
<div class="spacer">
    <div class="row">
		  <div class="col-12">
		    <h4 class="text-center">{{title}}</h4>
		  </div>
    </div>

    <div class="spacer-color row">
	<div class="col-12"></div>
    </div>
</div>
</template>

<script>
export default {
  props: ['title']
}
</script>

<style>

h4 {
  text-align: center;
}

h4::first-letter {
  margin: 0;
  padding:0;
}
h5::first-letter {
  margin: 0;
  padding:0;
}

.inner {
	width: 100%;
	margin: 0 auto;
	z-index: 1000;
	position:absolute;
	top: 50%;
}

.spacer {
  margin-top: 25px;
}

.spacer-color {
	background-color:#c4eeee;
	min-height:9px;
	margin-top: -18px;
	//position:absolute;
}

hr {
	border-width: 3px;
	border-color: black;
}
.letter {
  font-size: 100px;
  line-height: 0px;
}
.strut {
  display: inline-block;
  height: 100px;
}

</style>
