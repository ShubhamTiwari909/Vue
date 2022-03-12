<template>
  <div class="bg-stone-900 py-10 text-center">
    <input
      type="text"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      class="ring-2 ring-indigo-400 rounded px-3 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
    />

    <h1 class="my-5 text-slate-200">{{modelValue}}</h1>
  </div>
</template>

<script>
export default {
  name: "CompVModel",
  props: {
    modelValue: String,
  },
};
</script>

<style></style>
