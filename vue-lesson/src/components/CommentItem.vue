<template>
  <div>
    <div><b>Name: </b>{{ comment.name }}</div>
    <div><b>Email: </b>{{ comment.email }}</div>
    <div><b>Content: </b>{{ comment.content }}</div>
  </div>
  <div>
      <my-button class="btn btn-danger">Delete</my-button>
  </div>
</template>


<script>

export default {
    name: "my-comment-item",
    props: {
        comment: {
            type: Object,
            required: true
        }
    }
};
</script>