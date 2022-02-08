<template>
  <div :key="item.id" v-for="item in items">
      <Item :item="item" />
  </div>
</template>

<script>
import Item from './Item.vue'

export default {
 name: 'ListItems',
   components: {
    Item,
  },
 props:{
    items: Array,
 }
}
</script>

<style>

</style>