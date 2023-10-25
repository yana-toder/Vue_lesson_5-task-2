<template>
  <notebooks-panel :notebooks-cards-data="notebooksList" />
</template>

<script>
import notebooksPanel from './components/notebooksPanel.vue'

import {notebooksList} from './constants/3_data_notebooks'
export default {
  components: {notebooksPanel},
  name: 'App',

  data() {
    return {
      notebooksList,
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 50px;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
