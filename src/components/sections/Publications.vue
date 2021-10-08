<template>
    <resume-section title="Publications">
        <div slot="content">
          <div v-for='publication in publications'>
            <p class='publication'><a target="_blank" v-bind:href="'https://www.ncbi.nlm.nih.gov/pubmed/'+publication.pmid">{{publication.title}}</a></p>
            <p class="journal">
                <small>{{publication.journal}}</small>
            </p>
          </div>
        </div>
    </resume-section>
</template>

<script>
import resumeSection from './ResumeSection'
import publications from '../../data/publications.json'

export default {
  name: 'publications',
  data: function () { return publications },
  components: {
    resumeSection
  }
}
</script>

<style scoped>
  .publication {
    margin-bottom: 0px;
    margin-top: 7px;
  }
  .journal {
    margin-bottom: 5px;
  }
</style>
