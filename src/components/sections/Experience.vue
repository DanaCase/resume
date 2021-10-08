<template>
  <resume-section title="Experience">
    <div slot="content">
      <br/>
      <experienceSection  sectionTitle='Software Experience' v-bind:positions='positionSections.software' ></experienceSection>
      <experienceResearchSection  sectionTitle='Research Experience' v-bind:positions='positionSections.research' ></experienceResearchSection>
    </div>
  </resume-section>
</template>

<script>
import experience from '../../data/experience.json'
import resumeSection from './ResumeSection'
import experienceSection from './ExperienceSection'
import experienceResearchSection from './ExperienceResearchSection'

export default {
  name: 'experience',
  data: function () {
    return {positionSections: experience}
  },
  components: {
    resumeSection,
    experienceSection,
    experienceResearchSection
  }
}

</script>
