<template>
  <div class="bg-stone-900 py-48 text-center">
    <h1 class="bg-stone-200 text-2xl font-serif py-5">
      Computed: {{ getTotalComputed }}
    </h1>
    <h1 class="bg-stone-200 text-2xl font-serif py-5">
      Method: {{ getTotalMethod() }}
    </h1>
    <input
      class="bg-stone-200 my-10 ring-2 ring-red-500 rounded-md"
      type="text"
      v-model="name"
    />
    <!-- Difference between Method and Computed is method will re-render on every update
      while computed will re-render when their dependency get update or change-->

    <div class="bg-slate-100">
      <!-- using v-for with filter -->
      <h1>Using v-for with filter</h1>
      <h1 v-for="item in price" :key="item">
        <p v-if="item > 10">{{ item }}</p>
      </h1>

      <!-- using computer with filter -->
      <h1>Using computed with filter</h1>
      <h1 v-for="item in getPrice" :key="item">
        {{item}}
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "ComputedProp",
  data() {
    return {
      name: "",
      price: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15],
    };
  },
  methods: {
    getTotalMethod() {
      console.log("Method");
      return this.price.reduce((item, current) => (item = item + current), 0);
    },
  },
  computed: {
    getTotalComputed() {
      console.log("Computed");
      return this.price.reduce((item, current) => (item = item + current), 0);
    },
    getPrice() {
        return this.price.filter((item) => item > 10)
    }
  },
};
</script>

<style></style>
