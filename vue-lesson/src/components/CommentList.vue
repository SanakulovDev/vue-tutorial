<template>
  <div class="row align-items-center justify-content-center">
    <div
      class="col-md-6 border border-danger mr-2"
      v-for="comment in comments"
      v-bind:key="comment.id"
    >
      <p><b>Name: </b>{{ comment.name }}</p>
      <p><b>Email: </b>{{ comment.email }}</p>
      <p><b>Content: </b>{{ comment.content }}</p>
    </div>
  </div>
</template>

<script>
export default {
    props: {
        comments:{
            type: Array,
            required: true
        }
    }
};
</script>

<style scoped>
</style>