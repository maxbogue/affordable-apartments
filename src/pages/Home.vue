<template>
<div>
  <h1>STL Affordable Housing</h1>
  <div :class="$style.controls"></div>
  <div :class="$style.container">
    <results-list :results="results" />
    <results-map :results="results" />
  </div>
</div>
</template>

<script>
import ResultsList from '../components/ResultsList.vue';
import ResultsMap from '../components/ResultsMap.vue';

export default {
  components: {
    ResultsList,
    ResultsMap,
  },
  metaInfo: {
    title: 'Home',
  },
  data: () => ({
    // The results should be retrieved from the server.
    results: [{
      position: { lat:38.6524067, lng:-90.4377085 },
      text: 'test',
    }],
  }),
};
</script>

<style lang="scss" module>
.title {
  color: green;
}
.container {
  display: flex;
}
</style>
