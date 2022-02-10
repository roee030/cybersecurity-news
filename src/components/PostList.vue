<template>
  <div class="list_items_root" :key="item.id" v-for="item in items">
      <Post :item="item" />
  </div>
</template>

<script>
import Post from './Post.vue'

export default {
 name: 'ListItems',
   components: {
    Post,
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