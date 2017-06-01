<template>
<resume-section title="Education">
  <div slot="content">
	<span class="degree"><strong> M.S. Biological Chemistry </strong><br/></span>

	<span class="degree"><strong> B.S. Molecular, Cell, and Developmental Biology </strong></span>
  </div>
</resume-section>
</template>

<script>
import resumeSection from './ResumeSection'

export default {
  name: 'education',
  components: {
    resumeSection
  }
}
</script>
