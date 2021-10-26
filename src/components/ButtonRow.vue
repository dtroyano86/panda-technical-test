<template>
  <div class="button-row">
    <button>Sort By ID</button>
    <button>Sort By Priority</button>
    <select>
      <option :value="null">All Components</option>
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
