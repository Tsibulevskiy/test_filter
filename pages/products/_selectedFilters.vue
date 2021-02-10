<template>
  <h1>{{selectedFilters}}</h1>
</template>

<script>
export default {
  computed: {
    selectedFilters() {
      return this.$store.getters['filters/selectedFilters']
    }
  }
}
</script>

<style scoped>

</style>
