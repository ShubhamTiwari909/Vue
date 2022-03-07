<template>
  <div>
    <div class="bg-neutral-900 text-slate-200 text-center py-6 text-2xl">
      <h1>{{ volumes }}</h1>
      <button class="bg-green-700 px-5 py-2 rounded-md text-slate-200 mx-5 my-3" @click="volumes += 2">Increase volume</button>
      <button class="bg-red-700 px-5 py-2 rounded-md text-slate-200 mx-5 my-3" @click="volumes -= 2">Decrease volume</button>
    </div>
    <div class="bg-neutral-900 text-slate-900 text-center py-6 text-2xl">
      <input class="mx-5 p-2 rounded-md" type="text" v-model="App">
      <input class="mx-5 p-2 rounded-md" type="text" v-model="AppInfo.name">
      <input class="mx-5 p-2 rounded-md" type="text" v-model="AppInfo.version">
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
