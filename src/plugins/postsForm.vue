<template>
  <div>
    <form @submit.prevent="createNewPost">
      <input type="text" v-model="inputValue" :placeholder="placeholderInput" required>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  }
}
</script>

<style scoped>

</style>