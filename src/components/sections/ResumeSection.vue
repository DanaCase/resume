<template>
<div>
	<section-title :title="title"></section-title>
	<div class="row">
		<div class="m-x-auto">
			<slot name="content"></slot>
		</div>
	</div>
</div>
</template>

<script>
import sectionTitle from './SectionTitle'
export default {
  name: 'resume-section',
  props: ['title'],
  components: {
    sectionTitle
  }
}
</script>
