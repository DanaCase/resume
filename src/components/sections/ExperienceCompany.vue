<template>
    <div class='col-12 experienceCompany'>
        <div class='row companylink'>
            <div class='col-7 pull-left'>
                <strong> 
                    <a :href=position.link target="_blank">{{position.company}}</a>
                </strong>
            </div> 
        </div>
        <div class='row'>
            <div class='col-12 pull-left'>
                <experiencePosition v-for='(title, index) in position.titles' v-bind:key='index' :title='title'></experiencePosition>
            </div>
        </div>
    </div>
</template>

<script>
  import experiencePosition from './ExperiencePosition'

  export default {
    name: 'experienceCompany',
    props: ['position'],
    components: {
      experiencePosition
    }
  }
</script>

<style scoped>
a {
 color: #60A9E7;
}
</style>
