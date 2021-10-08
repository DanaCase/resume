<template>
      <div>
          <h5>{{sectionTitle}}</h5>
          <experienceResarchPosition v-for='(position, index) in positions' v-bind:key='index' v-bind:position='position' ></experienceResarchPosition>
      </div>
</template>

<script>
    import experienceResarchPosition from './ExperienceResearchPosition'

export default {
  name: 'experience',
  props: ['sectionTitle', 'positions'],
  components: {
        experienceResarchPosition
  }
}

</script>
