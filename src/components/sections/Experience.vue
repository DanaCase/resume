<template>
  <resume-section title="Experience">
    <div slot="content">
      <experiencePosition v-for='(position, index) in positions' v-bind:key='index' v-bind:position='position' ></experiencePosition>
    </div>
  </resume-section>
</template>

<script>
import resumeSection from './ResumeSection'
import experiencePosition from './ExperiencePosition'

export default {
  name: 'experience',
  data: function () {
    return {positions: myExperience}
  },
  components: {
    resumeSection,
    experiencePosition
  }
}

var myExperience = [{
  summary: 'Feel free to Vmake this information itemized instead of a paragraph. To adjust the heading lines and shading, select the text and choose “send to back”. Then, manipulate the lines. When you’re finished, select them and choose “send to back”. The text will be back in front again. From now on, the text will be replaced with Bob Ross Lorem Ipsum. Enjoy',
  date: 'Jan 2017 - present',
  position: 'Senior Software Engineer, Bioinformatics',
  company: 'Ambry Genetics'
}]
</script>
