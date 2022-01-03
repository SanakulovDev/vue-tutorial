<template>
  <div class="container">
    <div class="form mt-4">
      <form>
        <input
          :value="name"
          type="text"
          placeholder="Enter your name..."
          class="form-control"
        />
        <input
          :value="email"
          type="text"
          placeholder="Enter your email..."
          class="form-control my-4"
        />
        <input
          :value="content"
          type="text"
          placeholder="Enter your contents..."
          class="form-control"
        />
        <div class="d-flex flex-row-reverse">
          <button @click="createComponent" type="button" class="btn btn-primary mt-2">
            Add Comments
          </button>
        </div>
      </form>
    </div>
    <div class="row align-items-center justify-content-center">
      <div
        class="col-md-3 border border-danger mr-2"
        v-for="comment in comments"
      >
        <p><b>Name: </b>{{ comment.name }}</p>
        <p><b>Email: </b>{{ comment.email }}</p>
        <p><b>Content: </b>{{ comment.content }}</p>
      </div>
    </div>
  </div>
</template> 

<script>
export default {
  data() {
    return {
      comments: [
        { id: 1, name: "Home", email: "anvar@gmail.com", content: "123" },
        { id: 2, item: "About", email: "home@gmail.com", content: "dvkjdbv" },
      ],
      name: "",
      email: "",
      content: "",
    };
  },
  methods: {
    createComponent(){
      this.id = Date.now()
      // this.name = 
    },
  },
};
</script>

<style>
.begemot {
  width: 150px;
}
</style>