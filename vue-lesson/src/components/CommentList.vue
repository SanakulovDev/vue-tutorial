<template>
  <div class="row align-items-center justify-content-center">
    <div
      class="col-md-12 rounded my-2 comment"
      v-for="comment in comments"
      :key="comment.id"
>
  <comment-item :comment="comment" />
    </div>
  </div>
</template>

<script>
import CommentItem from './CommentItem.vue';

export default {

  components: {
    CommentItem
  },
    props: {
        comments:{
            type: Array,
            required: true
        }
    }
};
</script>

<style scoped>
.comment {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border: 5px solid rgb(109, 128, 209);
}
</style>