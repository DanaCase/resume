<template>
  <div class="container">
    <div class="row justify-content-md-center">
	<div class='col-auto'></div>
	<div class='col-lg-11'>
	  <div class="row contact">
 	    <div class ="col-4">
	      <hexagon></hexagon>
 	      <contact></contact>
          <publications></publications>
        </div>
	    <div class="col-8">
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
import publications from './sections/Publications'

export default {
  name: 'layout',
  components: {
    hexagon,
    contact,
    education,
    experience,
    publications
  }
}
</script>

<style>
/*.contact {
  position: fixed;
}*/
</style>
