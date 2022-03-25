<template>
  <div class="bg-stone-700 text-stone-200 py-10 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5">
    <h1 v-for="name in names" :key="name.firstname" class="place-self-center">
      <slot :firstname="name.firstname" :lastname="name.lastname"></slot>
    </h1>
  </div>
</template>

<script>
export default {
  name: "SlotProps",
  data() {
    return {
      names: [
        {
          firstname: "Shubham",
          lastname: "Tiwari",
        },
        {
          firstname: "Bharat",
          lastname: "Chauhan",
        },
        {
          firstname: "Abhishek",
          lastname: "Verma",
        },
      ],
    };
  },
};
</script>

<style></style>
