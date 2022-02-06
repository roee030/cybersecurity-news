<template>
  <div class="root_header">
    <Title />
    <Button label="New Post" icon="+" />
  </div>
</template>

<script>
import Title from './components/Title.vue'
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Title,
    Button
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
