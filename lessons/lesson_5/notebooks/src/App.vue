<template>
  <div class="itemsList">
    <list-item v-for="notebook in notebooksList" :key="notebook.id" :notebook="notebook" />
  </div>
</template>

<script>
import { notebooksList } from '@/constans/3_data_notebooks'
import ListItem from './components/ListItem.vue'
export default {
  name: 'App',
  components: { ListItem },

  computed: {
    notebooksList() {
      return notebooksList
    },
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

body {
  box-sizing: border-box;
}
</style>
