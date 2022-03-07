<template>
  <div>
    <h1>{{ id }}</h1>
    <h1>{{ name }}</h1>
    <h1>{{ email }}</h1>
  </div>
</template>

<script>
export default {
  name: "Props",
  props: {
    id:{
      type: Number,
      required: true,
      default: Math.floor(Math.random() * 1000000000)
    }, 
    name:{
      type: String,
      required: true,
      default: "None"
    },
   email:{
      type: String,
      required: true,
      default: "None"
    },
  }
};
</script>

<style></style>
