<template>
<div class='col-12'>
  <div class='row'>
    <div class='col-7 pull-left'>
     <strong> {{position.title}} </strong>
    </div> 
    <div class="col-5 pull-right text-right">
      {{position.dates}}
    </div>
  </div>
  <div class='row'>
    <div class='col-12 pull-left'>
	{{position.company}}
    </div>
  </div>
  <div class='row'>
    <div class="col-12">
        <div v-html="position.summary"></div>
    </div>
  </div>
  <div class='row'>
    <div class="col-12">
        <ul class='list-inline technology'>
         <li v-for='technology in position.technologies'>{{technology}}</li>
        </ul>
    </div>
  </div>
</div>
</template>

<script>
  export default {
    name: 'experiencePosition',
    props: ['position']
  }
</script>

<style>
    .technology > li{
        display: inline-block;
        padding-left: 5px;
    }
</style>
