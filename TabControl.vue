<template>
  <div class="bg-neutral-800 text-slate-300 py-20 text-center">
    <button v-bind:class="classButton + ' text-cyan-300 border-2 border-cyan-300'" @click="activeTab = 'TabA'">TabA</button>
    <button v-bind:class="classButton + ' text-indigo-300 border-2 border-indigo-300'" @click="activeTab = 'TabB'">TabB</button>
    <button v-bind:class="classButton + ' text-purple-500 border-2 border-purple-500'" @click="activeTab = 'TabC'">TabC</button>

    <!-- FIRST METHOD USING v-if -->
    <!-- <div>
        <TabA v-if="activeTab === 'TabA'" />
        <TabB v-if="activeTab === 'TabB'" />
        <TabC v-if="activeTab === 'TabC'" />
    </div> -->

    <!-- SECOND METHOD USING component tag-->
    <component :is="activeTab" />
  </div>
</template>

<script>
import TabA from './TabA.vue'
import TabB from './TabB.vue'
import TabC from './TabC.vue'
export default {
name:"TabControl",
components:{
    TabA,TabB,TabC
},
data() {
    return {
        activeTab : "TabA",
        classButton:"rounded-md px-5 py-2 mx-10"
    }
}
}
</script>

<style>

</style>