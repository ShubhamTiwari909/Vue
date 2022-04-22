<template>
  <div>
      <input type="text" ref="inputRefs" /> 
  </div>
</template>

<script>
export default {
name: "References-items",
mounted(){
  this.$refs.inputRefs.style.color = "red";
  this.$refs.inputRefs.style.borderColor = "cyan";
  this.$refs.inputRefs.focus();
}
}
</script>

<style>

</style>