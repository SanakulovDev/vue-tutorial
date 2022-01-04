<template>
  <div class="mt-4">
    <form @submit.prevent>
      <input
        v-model="comment.name"
        type="text"
        placeholder="Enter your name..."
        class="form-control"
      />
      <input
        v-model="comment.email"
        type="text"
        placeholder="Enter your email..."
        class="form-control my-4"
      />
      <input
        v-model="comment.content"
        type="text"
        placeholder="Enter your contents..."
        class="form-control"
      />
      <div class="d-flex flex-row-reverse my-3">
        <my-button @click="createComment" type="button" class="btn btn-primary">
          Add Comments
        </my-button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
     comment: {
        name: "",
        email: "",
        content: "",
      },
    };
  },
  methods: {
    createComment() {
      this.comment.id = Date.now();
      this.$emit("addComment", this.comment);
      this.comment = {
          name: '',
          email: '',
          content: ''
      }
    },
  },
};
</script>

<style scoped>
</style>