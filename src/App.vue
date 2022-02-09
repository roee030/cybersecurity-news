<template>
  <div v-bind:class="{ disabled: isModelOpen }">
    <div class="root_header">
      <Title />
      <Button @click="toggleNewPostModel" label="New Post" icon="+" />
    </div>
    <div class="root_list_items">
    <ListItems :items="items" />
    </div>
  </div>
    <div v-if="isModelOpen" class="new_post_model">
      <NewPost @toggle-new-post-model="toggleNewPostModel" />
    </div>
</template>

<script>
import Title from './components/Title.vue'
import Button from './components/Button.vue'
import ListItems from './components/ListItems.vue'
import NewPost from './components/NewPost.vue'

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
              {
                id:0,
                headLine:"IsTrickBot Indestructible?",
                tag:"vulnerabilities",
                description:"sadfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdfasdf",
                likes:0,
                comments:0,
                date:"January 30, 2021",
              },
          ],
          isModelOpen:true,
      }
  },
  methods: {
    toggleNewPostModel(){
      this.isModelOpen = !this.isModelOpen;
    }
  },
  components: {
    Title,
    Button,
    ListItems,
    NewPost,
  },
}
</script>

<style>
.root_header{
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
}

.root_list_items{
  margin-top: 50px;
}

.new_post_model{
    position: absolute;
    top: 73px;
    right: 50%;
    transform: translate(50%, 0px);
}

.disabled{
  opacity: 0.3;
}
</style>
