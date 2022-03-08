<template>
  <div>
    <h1 class="bg-gray-800 text-red-300 text-center text-3xl font-serif py-10">
      Provide and Inject method is used to pass down the data to the root level
      easily - <p class="text-indigo-400">{{ username }}</p>
    </h1>
  </div>
</template>

<script>
export default {
  name: "ProvideInject",
  inject: ["username"],
};
</script>

<style></style>
