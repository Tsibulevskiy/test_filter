<template>
  <div class="container mx-auto">
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 lg:flex lg:items-center lg:justify-center">
      <div class="mt-8 flex lg:mt-0 lg:flex-shrink-0">
        <div class="inline-flex rounded-md shadow">
          <nuxt-link to="/products/" class="inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700">
            Get product
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import filters from '~/components/filters'
export default {
  components: {
    filters
  }
}
</script>

<style>

</style>
