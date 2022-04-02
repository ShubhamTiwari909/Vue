<template>
  <div>
    <div>
      <button @click="getPosts()">{{ postVisible ? "Close Post" : "Load Post" }}</button>
    </div>
    <div v-show="postVisible">
        <div v-for="post in posts" :key="post.id">
        <h1>{{ post.ID }} {{ post.title }}</h1>
        <p>{{ post.body }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "GetPost",
  data() {
    return {
      posts: [],
      postVisible: false,
    };
  },
  methods: {
    getPosts() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => {
          this.posts = response.data;
        })
        .catch((err) => {
          console.log(err);
        });
      if (this.postVisible === true) {
        this.postVisible = false;
      } else {
        this.postVisible = true;
      }
    },
  },
};
</script>

<style></style>
