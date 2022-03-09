<template>
  <div class="app">
    <form class="form">
      <h4>Создание поста</h4>
      <input class="input" type="text" placeholder="Название">
      <input class="input" type="text" placeholder="Описание">
      <button class="btn">Создать</button>
    </form>
    <div class="post" v-for="post in posts">
      <div><strong>Название: </strong>{{post.title}}</div>
      <div><strong>Описание: </strong>{{post.body}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return{
      posts: [
        {id: 1, title: 'JS', body: 'Описание поста'},
        {id: 2, title: 'JS 2', body: 'Описание поста 2'},
        {id: 3, title: 'JS 3', body: 'Описание поста 3'}
      ]
    }
  },
  methods: {

  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app{
  padding: 20px;
}
.post{
  margin-top: 15px;
  padding: 20px;
  border: 2px solid green;
}
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