<template>
  <div class="component-obj">
    <pre>// Components</pre>
    <pre>{{ prettyComponents }}</pre>
  </div>
</template>

<script>
export default {
  name: 'ComponentObj',
  props: {
    components: Array
  },
  computed: {
    prettyComponents: function () {
      return JSON.stringify(this.components, null, 2)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .component-obj {
    background: lightgray;
    padding: 1rem;
    max-height: 300px;
    overflow: auto;
  }
</style>
