<template>
<div class='col-12 experiencePosition'>
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
	    <a :href=position.link target="_blank">{{position.company}}</a>
    </div>
  </div>
  <div class='row'>
      <div class="col-12">
          <div v-if="typeof position.summary === 'string'">
              <div v-html="position.summary"></div>
          </div>
          <div v-else >
              <div class='summary-row' v-for="value in position.summary">
                  {{ value }}
              </div>

          </div>
    </div>
  </div>
  <div class='row'>
    <div class="col-12">
        <ul class='list-inline technology'>
          <technology v-for='technology in position.technologies' :technologyName=technology>
            
          </technology>
        </ul>
    </div>
  </div>
</div>
</template>

<script>
  import technology from './Technology'

  export default {
    name: 'experienceResarchPosition',
    props: ['position'],
    components: {
      technology
    }
  }
</script>

<style scoped>
.summary-row {
    margin-bottom: 4px;
}
.experiencePosition {
    page-break-inside: avoid;
}
a {
 color: #60A9E7;
}
</style>
