<template>
  <div data-dynamic-dropdown>
    <input data-dynamic-dropdown-input
           v-model="value">
    </input>
    <div data-dropdown-options-wrapper
         v-for="option in results">
      <dropdown-option-card></dropdown-option-card>
    </div>
  </div>
</template>

<script>
  // no dropdown arrow, blank options to start
  // matching options only show up after typing one character
    // fuzzy search returns results if typed characters are found in any text inside the row-card component
  // options show up below input as row-cards (fake this component)
  // options are clickable and redirect after updating state

  import DropdownOptionCard from '../components/DropdownOptionCard.vue'

  module.exports = {
    name: 'DynamicDropdownMenu',
    components: {
      DropdownOptionCard
    },
    data() {
      return {
        results: null
      }
    },
    watch: {

    }
    computed() {
      
    },
  }
</script>

<style scoped>

</style>
