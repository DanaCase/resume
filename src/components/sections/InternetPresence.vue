<template>
  <resume-section title="Internet Presence" class='internet-presence'>
    <div slot="content">
      <div class='mini-spacer'>
      </div>
      <div v-for='site in links'>
        <div class='row site'>
          <div class="col-3">
            <i :class=site.icon></i>
          </div>
          <div class="col-9">
            <span class="align-middle">
              <a :href=site.link target="_blank">{{site.display}}</a>
            </span>
          </div>
        </div>
      </div>
    </div>
  </resume-section>
</template>

<script>
import resumeSection from './ResumeSection'

export default {
  name: 'internetPresence',
  data: function () {
    return {
      links: [
        {
          link: 'http://danacase.github.io',
          display: 'danacase.github.io',
          icon: 'fa fa-globe fa-2x'
        },
        {
          link: 'https://github.com/DanaCase',
          display: 'DanaCase',
          icon: 'fa fa-github fa-2x'
        },
        {
          link: 'https://www.linkedin.com/in/dana-l-case/',
          display: 'dana-l-case',
          icon: 'fa fa-linkedin fa-2x'
        },
        {
          link: 'https://stackoverflow.com/users/3637942/dana-case',
          display: 'dana case',
          icon: 'fa fa-stack-overflow fa-2x'
        }
      ]
    }
  },
  components: {
    resumeSection
  }
}
</script>

<style>

@media print {
  .internet-presence {
    page-break-inside: avoid;
  }
}

.mini-spacer {
  margin-top: 10px;
}

.site {
  margin-top: 5px;
}
</style>
