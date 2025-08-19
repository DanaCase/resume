<template>
  <div class="container">
    <div class="row justify-content-md-center">
	<div class='col-auto'></div>
  <div class='col-lg-11'>
    <div class="row content-row">
      <div class ="col-4 left-rail" ref="small">
        <div class="hex-area">
            <hexagon></hexagon>
          </div>
          <div class="sidebar-body">
            <contact></contact>
            <publications></publications>
            <internetPresence></internetPresence>
          </div>
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

@media print {
  .content-row {
    align-items: flex-start !important;
  }

  .left-rail {
    display: flex;
    flex-direction: column;
  }

  .sidebar-body {
    margin-top: auto;
    break-inside: auto;
    page-break-inside: auto;
  }

  .hex-area {
    display: flex;
    align-items: center;
    justify-content: center;
    break-inside: auto;
    page-break-inside: auto;
  }

  #hexagon {
    width: 100% !important;
    height: auto !important;
    max-height: 9cm;
  }
}
</style>
