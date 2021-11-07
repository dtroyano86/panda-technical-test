<template>
  <div class="component-list">
    <h1>Components</h1>

    <ButtonRow :components="components" v-on:set_sort="setSort" v-on:set_filter="setFilter" />

    <template v-for="component in updatedComponents" :key="component.id">
      <ComponentRow :component="component" />
    </template>
  </div>
</template>

<script>
import ComponentRow from './ComponentRow.vue'
import ButtonRow from './ButtonRow.vue'

export default {
  name: 'ComponentList',
  components: {
    ComponentRow,
    ButtonRow
  },
  props: {
    components: Array
  },
  data: () => ({
    sortBy: null,
    filterBy: null,
  }),
  computed: {
    updatedComponents: function() {
      let updated = [...this.components];
      if (this.sortBy) {
        updated.sort((a, b) => a[this.sortBy] - b[this.sortBy]);
      }
      if (this.filterBy) {
        updated = updated.filter((component) => component.type === this.filterBy);
      }
      return updated;
    },
  },
  methods: {
    setSort: function(sorter) {
      this.sortBy = sorter;
    },
    setFilter: function(filter) {
      this.filterBy = filter;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
