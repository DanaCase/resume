<template>
      <div>
          <h5>{{sectionTitle}}</h5>
          <experiencePosition v-for='(position, index) in positions' v-bind:key='index' v-bind:position='position' ></experiencePosition>
      </div>
</template>

<script>
import experiencePosition from './ExperiencePosition'

export default {
  name: 'experience',
  props: ['sectionTitle', 'positions'],
  components: {
    experiencePosition
  }
}

</script>
