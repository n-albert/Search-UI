<script setup>
  import FullPageHeader from '@/components/FullPageHeader.vue';
  import ResultsSidebar from '@/components/ResultsSidebar.vue';
  import ResultsContent from '@/components/ResultsContent.vue';
</script>

<template>
    <FullPageHeader />
    <div class="results-container">
      <ResultsSidebar />
      <ResultsContent msg="This is the results page. It is still in progress."/>
    </div> 
</template>


<style>
  body {
    place-items: start;
  }
  .results-container {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
  }
  @media (min-width: 512px) {
    body {
      place-items: start;
    }
  }
</style>
  