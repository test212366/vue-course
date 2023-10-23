<template>
  <main>
    <posts-form :inputValue="inputValue"/>
      <posts :posts="posts"/>

  </main>
</template>

<script>
import postsForm from "@/plugins/postsForm";
import posts from "@/plugins/posts";
  export default {
    components: {
      posts,postsForm
    },
    data() {
      return {
        posts: [
          {id: 1, title: 'js', body: 'desc'},
          {id: 2, title: 'js2', body: 'desc'},
          {id: 3, title: 'js3', body: 'desc'}
        ],
        inputValue:'',
        currentId: 3,
        placeholderInput: 'Введите title:'
      }
    },
    methods: {
      createNewPost() {
        this.currentId++
        this.posts.push({id: this.currentId, title: this.inputValue, body: 'none'})
        this.inputValue = ''
      }
    }
  }

</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  input {
    font-size: 20px;
    margin: 20px;
    padding: 10px;
  }
  #app {
    margin: 5px;
  }
</style>