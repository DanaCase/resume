<template>
<div>
  <div class='row'>
    <div class='col-4 pull-left'>
      {{position.position}}
    </div> 
    <div class="col-8 pull-right">
      {{position.date}}
    </div>
  </div>
  <div class='row'>
    <div class='col-12 pull-left'>
	{{position.company}}
    </div>
  </div>
  <div class='row'>
    {{position.summary}}
  </div>
</div>
</template>

<script>
  export default {
    name: 'experiencePosition',
    props: ['position']
  }
</script>
