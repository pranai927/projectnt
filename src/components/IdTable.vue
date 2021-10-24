<template>
  <div class="container">
   <div class="row">
  <table class="table">
    <thead>
      <tr>
        <th scope="col">User_id</th>
        <th scope="col">id</th>
        <th scope="col">Title</th>
        <th scope="col">Body</th>
       
      </tr>
    </thead>
    <tbody>
      <tr v-for="post in posts" v-bind:key="post.id">
        <th scope="row"><div>{{ post.userId }}</div></th>
        <td> <div>{{ post.id }}</div></td>
        <td><h2>{{ post.title }}</h2></td>
        <td> <div>{{ post.body }}</div></td>
      </tr>
    
    </tbody>
  </table>
    </div>
 </div>
</template>

<script>
export default {
  name: "IdTable",
  props: {
    msg: String,
  },
  data() {
    return {
      posts: [],
    };
  },

  methods: {
    async getData() {
      try {
        const response = await this.$http.get(
          "https://jsonplaceholder.typicode.com/posts?id=1"
        );
        // JSON responses are automatically parsed.
        this.posts = response.data;
         
      } catch (error) {
        console.log(error);
      }
      
    },
  },

  created() {
    this.getData();
  },
};
</script>