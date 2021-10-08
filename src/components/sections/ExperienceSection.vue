<template>
      <div>
          <h5>{{sectionTitle}}</h5>
          <experienceCompany v-for='(position, index) in positions' v-bind:key='index' v-bind:position='position'></experienceCompany>
          <!--<experiencePosition v-for='(position, index) in positions' v-bind:key='index' v-bind:position='position' ></experiencePosition>-->
      </div>
</template>

<script>
import experienceCompany from './ExperienceCompany'

export default {
  name: 'experience',
  props: ['sectionTitle', 'positions'],
  components: {
    experienceCompany
  }
}

</script>

