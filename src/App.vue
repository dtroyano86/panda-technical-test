<template>
  <img id="logo" alt="Vue logo" src="./assets/logo.png">
  <ComponentObj :components="components"/>
  <ComponentList :components="components"/>
</template>

<script>
import ComponentList from './components/ComponentList.vue'
import ComponentObj from './components/ComponentObj.vue'

export default {
  name: 'App',
  components: {
    ComponentList,
    ComponentObj
  },
  data: () => {
    return {
      components: [
        {
          id: 1234,
          name: 'Attack Cards',
          type: 'cards',
          priority: 7
        },
        {
          id: 325,
          name: 'D6',
          type: 'dice',
          priority: 6
        },
        {
          id: 554,
          name: 'D20',
          type: 'dice',
          priority: 16
        },
        {
          id: 892,
          name: 'Rule Booklet',
          type: 'booklet',
          priority: 15
        },
        {
          id: 12,
          name: 'Wooden Sheep',
          type: 'wood',
          priority: 5
        },
        {
          id: 93,
          name: 'Rocket Ship',
          type: 'plastic',
          priority: 8
        },
        {
          id: 34,
          name: 'Game Box',
          type: 'box',
          priority: 1
        },
        {
          id: 27,
          name: 'Box sleeve',
          type: 'sleeve',
          priority: 2
        },
        {
          id: 938,
          name: 'Score sheets',
          type: 'paperPad',
          priority: 9
        },
        {
          id: 9378,
          name: 'D10',
          type: 'dice',
          priority: 4
        },
        {
          id: 89,
          name: 'Damage Cards',
          type: 'cards',
          priority: 14
        },
        {
          id: 876,
          name: 'Plastic Tray',
          type: 'tray',
          priority: 3
        },
        {
          id: 39,
          name: 'Zip lock bags',
          type: 'zipLock',
          priority: 10
        },
        {
          id: 22,
          name: 'Wooden Meeples',
          type: 'wood',
          priority: 11
        },
        {
          id: 234,
          name: 'Plastic Goblet',
          type: 'plastic',
          priority: 17
        },
        {
          id: 3456,
          name: 'Acrylic Tiles',
          type: 'tiles',
          priority: 13
        },
        {
          id: 43,
          name: 'Player Mats',
          type: 'cardboard',
          priority: 18
        },
        {
          id: 376,
          name: 'Player Guide',
          type: 'booklet',
          priority: 12
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  width: 80vw;
  margin: auto;
}

#logo {
  max-height: 100px;
  margin: 3rem auto;
  display: block;
}

</style>
