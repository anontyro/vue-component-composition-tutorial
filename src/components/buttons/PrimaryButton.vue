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
@import '@/assets/css/mixins.scss';
$bgColor: #2196f3;
.primary-btn {
  @include base-button-setup($bgColor);
  background-color: $bgColor;
  color: white;
}
</style>
