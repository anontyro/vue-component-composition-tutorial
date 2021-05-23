<template>
  <div class="main-container">
    <div class="header-section">
      <slot name="header">Header</slot>
    </div>
    <div class="main-body">
      <slot>Body is default</slot>
    </div>
    <div class="footer-section">
      <slot name="footer">footer section</slot>
    </div>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
export default defineComponent({
  name: 'BaseContainer',
});
</script>

<style lang="scss" scoped>
.main-container {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  height: 800px;
  margin: 10px auto;
  border: 1px solid #d9d9d9;
  border-radius: 5px;
}

.header-section {
  border-bottom: 1px solid #d9d9d9;
}

.footer-section {
  border-top: 1px solid #d9d9d9;
}

.main-body {
  display: flex;
  flex-grow: 1;
}
</style>
