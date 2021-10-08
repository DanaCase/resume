<template>
<!--<div class='col-12 experiencePosition'>-->
<div class='experiencePosition'>
<div class='row'>
    <div class='col-7 pull-left'>
     <strong> {{title.title}} </strong>
    </div> 
    <div class="col-5 pull-right text-right">
      {{title.dates}}
    </div>
  </div>
  <div class='row'>
      <div class="col-12">
          <div v-if="typeof title.summary === 'string'">
              <div v-html="title.summary"></div>
          </div>
          <div v-else >
              <div class='summary-row' v-for="value in title.summary">
                  {{ value }}
              </div>

          </div>
    </div>
  </div>
  <div class='row'>
    <div class="col-12">
        <ul class='list-inline technology'>
          <technology v-for='technology in title.technologies' :technologyName=technology>
            
          </technology>
        </ul>
    </div>
  </div>
</div>
</template>

<script>
  import technology from './Technology'

  export default {
    name: 'experiencePosition',
    props: ['title'],
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
</style>
