<template>
  <div class="post">
    <div>
      <div><strong>Название: </strong>{{post.title}}</div>
      <div><strong>Описание: </strong>{{post.body}}</div>
    </div>
    <div class="post-btns">
      <button>Удалить</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
.post{
  margin-top: 15px;
  padding: 20px;
  border: 2px solid green;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.post-btns{
  /* TODO:50:00 */

}
</style>