<template>
  <div class="component-row">
    <h3>{{ component.name }} ({{ component.type }})</h3>
    <span class="component-id">ID: {{ component.id }}</span>
    <span class="component-priority">Priority: {{ component.priority }}</span>
  </div>
</template>

<script>
export default {
  name: 'ComponentRow',
  props: {
    component: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .component-row {
    box-shadow: 0 0 2px 2px rgba(0, 0, 0, .1);
    padding: .5rem;
    border-radius: 4px;
    margin-bottom: 1rem;
    position: relative;
  }

  h3 {
    margin: 0
  }

  span {
    position: absolute;
    top: .75rem;
    right: .5rem;
  }

  .component-priority {
    right: 6rem;
  }
</style>
