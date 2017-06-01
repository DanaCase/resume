<template>
  <div class="container">
    <div class="row justify-content-md-center">
	<div class='col-auto'></div>
	<div class='col-lg-11'>
	  <div class="row">
 	    <div class ="col-3">
	      <hexagon></hexagon>
 	      <contact></contact>
	    </div>
	    <div class="col-9">
	      <education></education>
	      <experience></experience>
	    </div>
	  </div>  
	</div>
	<div class='col-auto'></div> 
    </div>
  </div>
</template>

<script>

import hexagon from './Hexagon'
import contact from './Contact'

import education from './sections/Education'
import experience from './sections/Experience'

export default {
  name: 'layout',
  components: {
    hexagon,
    contact,
    education,
    experience
  }
}
</script>
