<template>
<div class="spacer">
    <div class="row">
	<div class="col-xs-4">
	    <hr/>
	    <div class=""></div>
	</div>
	<div class="col-xs-4">
		<h4 class="text-xs-center">{{title}}</h4>
	</div>
	<div class="col-xs-4">
	    <hr/>
	</div>
    </div>

    <div class="spacer-color row">
	<div class="col-xs-12"></div>
    </div>
</div>
</template>

<script>
export default {
  props: ['title']
}
</script>

<style>

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
</style>
