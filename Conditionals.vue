<template>
  <div>
    <!-- if elseif else -->
    <div>
      <h1 v-if="name === 'Shubham'">Name is {{ name }}</h1>
      <h1 v-else-if="name === 'Bharat'">Name is {{ name }}</h1>
      <h1 v-else>Name is not found</h1>
    </div>

    <!-- using v-if -->
    <div v-if="display">
      <h1>This will display if the display is true</h1>
    </div>
    <!-- using v-show -->
    <div v-show="display">
      <h1>This will display if the display is true</h1>
    </div>
    <div>
      <h1>Name is {{ name }}</h1>
      <button @click="changeName('Abhishek')">Change</button>
    </div>
    <div class="bg-neutral-900 text-slate-200 py-6 text-center text-3xl font-mono">
      <h1>Original Numbers are {{ numbers }}</h1>
      <h1>Filter Numbers are {{ filterNumbers }}</h1>
      <h1>{{error}} </h1>
      <button @click="filterNumber(numbers)">Change</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Conditionals",
  data() {
    return {
      name: "Bharat",
      display: true,
      numbers: [1, 3, 5, 7, 9, 11, 12, 13, 14, 15, 16, 17, 18],
      filterNumbers: [],
      error:""
    };
  },
  methods: {
    changeName(name) {
      if (this.name == name) {
        this.name = "Shubham";
      } else {
        this.name = name;
      }
    },
    filterNumber(array) {
      let userInput = parseInt(prompt("Enter a number"));
      let filtered = array.filter((item) => item > userInput);
      if (this.filterNumbers.length >= 0 && !isNaN(userInput)) {
        this.filterNumbers = filtered;
        this.error = ""
      }
      else{
        this.error = "Please enter a number to filter the array"
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dark {
  text-align: center;
  color: aliceblue;
}
</style>
