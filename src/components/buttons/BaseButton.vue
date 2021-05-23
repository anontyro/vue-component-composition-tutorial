<template>
  <button
    :type="type"
    :class="btnClass ?? 'base-button'"
    @click="$router.push(to)"
  >
    <slot>Test</slot>
  </button>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
export default defineComponent({
  name: 'BaseButton',
  props: {
    to: String,
    btnClass: String,
    type: {
      type: String,
      default: 'button',
    },
  },
  created() {
    console.log(this.to);
  },
});
</script>

<style lang="scss" scoped></style>
