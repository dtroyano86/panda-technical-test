<template>
  <div class="component-list">
    <h1>Components</h1>

    <ButtonRow :components="components" />

    <template v-for="component in components" :key="component.id">
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
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
