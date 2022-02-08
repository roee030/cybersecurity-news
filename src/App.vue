<template>
  <div class="root_header">
    <Title />
    <Button label="New Post" icon="+" />
  </div>
  <ListItems :items="items" />
</template>

<script>
import Title from './components/Title.vue'
import Button from './components/Button.vue'
import ListItems from './components/ListItems.vue'

export default {
  name: 'App',
    data(){
      return{
          items: [
              {
                id:0,
                headLine:"IsTrickBot Indestructible?",
                tag:"vulnerabilities",
                description:"sadfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdf",
                likes:0,
                comments:0,
                date:"January 30, 2021",
              },
          ]
      }
  },
  components: {
    Title,
    Button,
    ListItems
  }
}
</script>

<style>
.root_header{
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>
