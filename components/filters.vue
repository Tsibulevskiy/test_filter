<template>
  <div class="flex flex-row flex-wrap justify-center">
    <fieldset v-for="(type, i) in filters" :key="i">
      <div class="bg-purple-300 rounded p-1.5 m-1.5" >
        <div>
          <legend class="text-center font-medium text-gray-900">{{type.title}}</legend>
        </div>
        <div class="mt-4 space-y-4" v-for="(value, number) in type.values" :key="number">
          <div class="flex items-center pr-3 pl-3">
            <input  :id="type.title" :name="type.title" :type="type.type"
                    class="focus:ring-indigo-500 h-4 w-4 text-indigo-600 border-gray-300"
                    @change="filtered(value)">
            <label  :for="type.title" class="ml-3 block text-sm font-medium text-gray-700">
              {{ value.title }}
            </label>
          </div>
        </div>
      </div>
    </fieldset>
    <br>{{ selectedFilters }}
  </div>
</template>

<script>
export default {
  computed: {
    filters() {
      return this.$store.getters['filters/getTypes'].filter(item => {
        return item
      })
    },
    selectedFilters() {
      return this.$store.getters['filters/getSelectedFilters']
    }
  },
  methods: {
    filtered(value) {
      console.log(value)
      this.$store.commit('filters/selectedFilters', value)
    }
  }
}
</script>

<style scoped>

</style>
