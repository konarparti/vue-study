<template>
  <div>
    <h3>Список</h3>
    <post-item :post="post" v-for="post in posts"/>
  </div>

</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  components: {PostItem},
  props:{
    posts:{
      type: Array,
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
}
</style>