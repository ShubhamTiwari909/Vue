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
  </div>
</template>

<script>
export default {
  name: "Conditionals",
  data() {
    return {
      name: "Bharat",
      display:true,

    };
  },
  methods: {
    changeName(name) {
      if(this.name == name)
      {
        this.name = "Shubham";
      }
      else{
        this.name = name;
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dark {
  text-align: center;
  color: aliceblue;
}
</style>
