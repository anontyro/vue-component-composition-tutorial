<template>
  <BaseLink classOverload="primary-btn" @click="onClick">
    <span>{{ title }}</span>
  </BaseLink>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseLink from './BaseLink.vue';

export default defineComponent({
  name: 'PrimaryButton',
  components: {
    BaseLink,
  },
  props: {
    onClick: {
      type: Function,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped>
.primary-btn {
  min-width: 75px;
  display: inline-block;
  margin: 10px;
  border: 1px solid black;
  border-radius: 10px;
  padding: 3px;
  font-weight: 700;
  font-size: 1.2rem;
  &:hover {
    background-color: darken(white, 5%);
  }
}
</style>
