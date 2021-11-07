<template>
  <div class="button-row">
    <button @click="sortById">Sort By ID</button>
    <button @click="sortByPriority">Sort By Priority</button>
    <select @change="selectFilter($event)">
      <option value="">All Components</option>
      <option v-for="type in componentTypes" :key="type" :value="type">{{ type }}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'ButtonRow',
  props: {
    components: Array
  },
  computed: {
    componentTypes: function () {
      let types = [...new Set(this.components.map(c => c.type))]
      console.log(types)
      return types
    }
  },
  methods: {
    sortById: function () {
      this.$emit('set_sort', 'id');
    },
    sortByPriority: function () {
      this.$emit('set_sort', 'priority');
    },
    selectFilter: function (e) {
      const type = !e.target.value.length ? null : e.target.value
      this.$emit('set_filter', type);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .button-row {
    margin-bottom: 2rem;
  }

  button {
    margin-right: 1rem;
  }
</style>
