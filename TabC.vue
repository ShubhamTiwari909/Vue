<template>
  <div class="text-purple-600 my-10 text-xl">
      <h1>This is TAB C</h1>
      <input type="text" v-model="name" class="ring-2 ring-purple-400 rounded-md px-2.5 py-2 my-10">
  </div>
</template>

<script>
export default {
name:"TabC",
data() {
  return{
    name:""
  }
}
}
</script>

<style>

</style>