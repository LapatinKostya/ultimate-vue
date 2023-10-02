<template>
  <div class="app">
    <post-form :title="title" :body="body"/>
    <post-list :posts="posts"/>

  </div>
</template>

<script>
import PostForm from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";

export default {
  components: {
    PostForm,
    PostList
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Vue 1', body: 'Описание 1'},
        {id: 2, title: 'Vue 2', body: 'Описание 2'},
        {id: 3, title: 'Vue 3', body: 'Описание 3'},
        {id: 4, title: 'Vue 4', body: 'Описание 4'},
        {id: 5, title: 'Vue 5', body: 'Описание 5'},
      ],
      title: '',
      body: '',
    }
  },
  methods: {}
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}

form {
  display: flex;
  flex-direction: column;
}

.input {
  width: 100%;
  border: 2px solid #41b784;
  margin-bottom: 20px;
  height: 40px;
  padding: 5px;
}

.btn {
  align-self: flex-end;
  padding: 5px;
  background: none;
  color: #34485d;
  border: 2px solid #34485d;
}
</style>
