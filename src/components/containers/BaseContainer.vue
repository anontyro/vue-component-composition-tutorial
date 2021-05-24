<template>
  <div class="main-container">
    <div class="header-section" v-if="hasHeaderSlot">
      <slot name="header"></slot>
    </div>
    <div class="main-body">
      <slot></slot>
    </div>
    <div class="footer-section" v-if="hasFooterSlot">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
export default defineComponent({
  name: 'BaseContainer',
  computed: {
    hasHeaderSlot() {
      return !!this.$slots.header;
    },
    hasFooterSlot() {
      return !!this.$slots.footer;
    },
  },
});
</script>

<style lang="scss" scoped>
.main-container {
  display: flex;
  flex-direction: column;
  width: 500px;
  height: 500px;
  margin: 10px;
  border: 1px solid #d9d9d9;
  overflow: hidden;
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
  overflow: hidden;
}
</style>
