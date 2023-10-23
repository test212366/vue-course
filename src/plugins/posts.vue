<template>
    <div className="post" v-for="post in posts">
      <div><strong>Название: {{post.title}} </strong> Описание: {{post.body}}</div>
    </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid #000;
  margin-top: 20px;
}
</style>