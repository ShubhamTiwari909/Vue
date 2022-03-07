<template>
  <div>
    <div>
      <h1>{{ volumes }}</h1>
      <button @click="volumes += 2">Increase volume</button>
      <button @click="volumes -= 2">Decrease volume</button>
    </div>
    <div>
      <input type="text" v-model="App">
      <input type="text" v-model="AppInfo.name">
      <input type="text" v-model="AppInfo.version">
    </div>
  </div>
</template>

<script>
export default {
  name: "Watchers",
  data() {
    return {
      volumes: 0,
      App: "BGMI",
      AppInfo: {
          name:"BGMI",
          version:"3.9.11"
      }
    };
  },
  methods: {},
  computed: {},
  watch: {
    // simple watcher
    volumes(newValue, oldValue) {
      if (newValue > oldValue && newValue === 14) {
        alert("Too much volume");
      }
    },
    App: {
        handler(newValue){
            console.log(newValue)
        },
        immediate: true//to call the method when the page is loaded
    }, 
    AppInfo: {
        handler(newValue){
            console.log(newValue.name + " " + newValue.version)
        },
        deep: true//to call the method for the objects data and array data
    }
  },
};
</script>

<style></style>
