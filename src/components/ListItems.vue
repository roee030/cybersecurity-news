<template>
  <div class="list_items_root" :key="item.id" v-for="item in items">
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
    .list_items_root{
        background-color:white;
        width: 930px;
        margin: 0 auto;
    }
</style>