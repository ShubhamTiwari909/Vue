<template>
  <div>
    <h1 class="bg bg-slate-900 text-center text-4xl text-indigo-400 py-5">
      Hello {{name}}
    </h1>
    <h1 v-html="bindingHtml"></h1>
    <h1 v-bind:id="heading" v-bind:class="[bindedClass,tailwindClass]">Binded Class</h1>
    <h1 v-bind:class="isDisabled ? 'text-green-600' : 'text-red-700'">Binding conditional</h1>
    <h1 v-bind:class="[isDisabled ? 'text-green-600' : 'text-red-300',tailwindClass]">Binding conditional</h1>
    <button v-bind:disabled="isDisabled">Disabled</button>
  </div>
</template>

<script>
export default {
  name: "Basic",
 data() {
   return {
     name : "Shubham",
     bindingHtml: "<p class='text-red-800'>Hello Everyone</p>",
     heading: "Heading",
     isDisabled : false,
     bindedClass : "dark",
     tailwindClass : "py-5 bg-slate-700"
   }
 }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dark{
  text-align:center;
  color: aliceblue;
}
</style>
