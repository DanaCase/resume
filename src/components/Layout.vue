<template>
  <div class="container">
    <div class="row justify-content-md-center">
	<div class='col-auto'></div>
  <div class='col-lg-11'>
    <div class="row">
      <div class ="col-4" ref="small">
          <hexagon></hexagon>
          <contact></contact>
        <publications></publications>
        <internetPresence></internetPresence>  
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
import internetPresence from './sections/InternetPresence'

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
    publications,
    internetPresence
  }
}
</script>

<style>
</style>
