<template>
  <div class="bg-slate-800 py-5 my-10">
      <h1 class="text-center text-slate-200 py-5 text-2xl my-5">This is a Popup</h1>
      <button class="bg-gradient-to-r from-red-200 via-red-300 to-red-400 px-5 py-2 rounded-md"
       @click="$emit('close')">Close Popup</button>
  </div>
</template>

<script>
export default {
name:"Popup",
emits:["close"]
}
</script>

<style>

</style>