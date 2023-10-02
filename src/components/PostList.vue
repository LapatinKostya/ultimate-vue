<template>
  <div class="post" v-for="post in posts">
    <div>Название: {{ post.title }}</div>
    <div>Описание: {{ post.body }}</div>
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
  border: 3px solid #41b784;
  padding: 5px;
  margin-top: 20px;
}
</style>
