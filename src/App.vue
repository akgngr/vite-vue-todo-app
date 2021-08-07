<template>
  <div class="container w-11/12 lg:w-6/12 m-auto">
    <h1 class="font-bold text-center py-2 pt-4">TODO List</h1>
    <hr />
    <add-item />
    <list-item />
    <count-list />
  </div>
</template>

<script>
import addItem from './components/addItem.vue';
import countList from './components/countList.vue'
import listItem from './components/listItem.vue'

export default {
  data(){
    return{
      provideData: {
        data: [
          { id: 1, title: 'Vue 3 Bootcamp #1' },
          { id: 2, title: 'Vue 3 Bootcamp #2' },
          { id: 3, title: 'Vue 3 Bootcamp #3' },
          { id: 4, title: 'Vue 3 Bootcamp #4' },
          { id: 5, title: 'Vue 3 Bootcamp #5' },
          { id: 6, title: 'Vue 3 Bootcamp #6' },
          { id: 7, title: 'Vue 3 Bootcamp #7' },
          { id: 8, title: 'Vue 3 Bootcamp #8' },
          { id: 9, title: 'Vue 3 Bootcamp #9' },
          { id: 10, title: 'Vue 3 Bootcamp #10' }
        ]
      }
    }
  },
  components: {
    addItem,
    countList,
    listItem
  },
  provide() {
    return{
        pushItem: this.pushItem,
        itemData: this.provideData,
        deleteItem: this.deleteItem
      }
  },
  methods: {
    pushItem(event){
      this.provideData.data.push({
        id: new Date().getTime(),
        title: event
      })
    },
    deleteItem(event){
      this.provideData.data = this.provideData.data.filter(t => t !== event)
    }
  }
}

</script>

<style>
</style>
