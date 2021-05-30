<template>
  <BaseLink classOverload="secondary-btn" @click="onClick">
    <span>{{ title }}</span>
  </BaseLink>
</template>

<script lang="ts">
import Vue, {defineComponent} from 'vue';
import BaseLink from './BaseLink.vue';

export default defineComponent({
  name: 'SecondaryButton',
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
.secondary-btn {
  @include base-button-setup;
}
</style>
