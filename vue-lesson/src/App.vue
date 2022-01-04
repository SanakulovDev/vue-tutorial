<template>
  <div class="container">
    <comment-form @addComment="createComment" />
    <comment-list :comments="comments" />
  </div>
</template> 

<script>
import CommentForm from "./components/CommentForm";
import CommentList from "./components/CommentList";

export default {
  components: {
    CommentForm,
    CommentList
  },
  data() {
    return {
      comments: [
        { id: 1, name: "Home", email: "anvar@gmail.com", content: "123" },
        { id: 2, item: "About", email: "home@gmail.com", content: "dvkjdbv" },
      ],
     
    };
  },
  methods: {
    createComment(comment) {
      this.comments.push(comment)
    },
    
  },
};
</script>

<style>
.begemot {
  width: 150px;
}
</style>