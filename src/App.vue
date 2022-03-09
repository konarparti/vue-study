<template>
  <div class="app">
    <post-form>

    </post-form>
    <post-list :posts="posts"> <!--тоже самое что и v-bind:posts="posts"-->

    </post-list>
  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";
export default {
  components:{
    PostList, PostForm
  },
  data() {
    return{
      posts: [
        {id: 1, title: 'JS', body: 'Описание поста'},
        {id: 2, title: 'JS 2', body: 'Описание поста 2'},
        {id: 3, title: 'JS 3', body: 'Описание поста 3'}
      ],
      title: '',
      body: ''
    }
  },
  methods: {
    createPost(){
      const newPost ={
        id: Date.now(),
        title: this.title,
        body: this.body,
      }
      this.posts.push(newPost);
      this.title = '';
      this.body = '';
    }
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
</style>