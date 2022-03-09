<template>
  <div>
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

.post{
  margin-top: 15px;
  padding: 20px;
  border: 2px solid green;
}
</style>