<template xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <form @submit.prevent>
    <input
        v-bind:value="title"
        @input="title = $event.target.value"
        class="input"
        type="text"
        placeholder="Название"
    >
    <input
        v-bind:value="body"
        @input="body = $event.target.value"
        class="input"
        type="text"
        placeholder="Описание"
    >
    <button class="btn" @click="createPost">Создать пост</button>
  </form>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    body: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
