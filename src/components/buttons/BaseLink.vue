<template>
  <div :class="`link-item ${classOverload}`" @click="onClick">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import Vue, {defineComponent} from 'vue';
export default defineComponent({
  name: 'BaseLink',
  props: {
    onClick: {
      type: Function,
      required: true,
    },
    classOverload: {
      type: String,
      default: '',
    },
  },
});
</script>

<style lang="scss" scoped>
.link-item {
  cursor: pointer;
  padding: 10px;
  &:hover {
    color: darken(#2c3e50, 10%);
  }
}
</style>
