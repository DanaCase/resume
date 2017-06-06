<template>
  <li class="technologyItem">
    {{technologyName}}
  </li>
</template>

<script>
  
  export default {
    name: 'technology',
    props: ['technologyName']
  }

</script>

<style>
  .technologyItem {
    background-color:#c4eeee;
    color: #4f7a80;
    display: inline-block;
    padding: 0px 5px 0px 5px;
    margin-right: 5px;
    margin-top: 1px;
  }
</style>
