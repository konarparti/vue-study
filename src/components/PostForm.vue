<template>
  <div class="app">
    <form class="form" @submit.prevent>
      <h4>Создание поста</h4>
      <input v-bind:value="title" @input="title = $event.target.value" class="input" type="text" placeholder="Название">
      <input v-bind:value="body" @input="body = $event.target.value" class="input" type="text" placeholder="Описание">
      <button class="btn" @click="createPost">Создать</button>
    </form>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.form {
  display: flex;
  flex-direction: column;
}
.btn{
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
.input{
  width: 100%;
  border: 1px solid teal;
  padding: 10px;
  margin-top: 15px;
}
</style>