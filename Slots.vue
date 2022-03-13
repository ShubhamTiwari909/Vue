<template>
  <div>
      <!-- Normal slots -->
      <!-- <div>
        <slot>This is the Default Value of slot tag</slot>
      </div> -->
      <!-- Named slots -->
      <div>
          <div>
              <slot name="Header"></slot>
          </div>
          <div>
              <slot name="Content"></slot>
          </div>
          <div>
              <slot name="Footer"></slot>
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>