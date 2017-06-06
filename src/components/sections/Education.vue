<template>
<resume-section title="Education">
  <div slot="content">
	<div class="row">
	  <div class="col-12">
	    <span class="degree"><strong> M.S. Biological Chemistry </strong><br/></span>
	  </div>
	</div>

	<div class="row">
	  <div class="col-12">
      <span class="degree">University of California Los Angeles <br/></span>
	  </div>
	</div>
  <div class="row">
    <div class="col-12">
      <span class="degree"><strong> B.S. Molecular, Cell, and Developmental Biology <em>cum laude</em></strong></span>
    </div>
  </div>
	<div class="row">
	  <div class="col-12">
	    <span class="degree">University of California Los Angeles<br/></span>
	  </div>
	</div>
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
