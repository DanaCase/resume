<template>
  <resume-section title="Experience">
    <div slot="content">
      <experienceSection  sectionTitle='Software Experience' v-bind:positions='positionSections.software' ></experienceSection>
      <experienceSection  sectionTitle='Research Experience' v-bind:positions='positionSections.research' ></experienceSection>
    </div>
  </resume-section>
</template>

<script>
import experience from '../../data/experience.json'
import resumeSection from './ResumeSection'
import experienceSection from './ExperienceSection'

export default {
  name: 'experience',
  data: function () {
    return {positionSections: experience}
  },
  components: {
    resumeSection,
    experienceSection
  }
}

</script>
