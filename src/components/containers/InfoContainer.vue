<template>
  <BaseContainer>
    <template v-slot:header>
      <h1>{{ title }}</h1>
    </template>
    <div class="text-content">
      <slot></slot>
    </div>
  </BaseContainer>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseContainer from './BaseContainer.vue';

export default defineComponent({
  name: 'InfoContainer',
  components: {
    BaseContainer,
  },
  props: {
    title: String,
  },
});
</script>

<style lang="scss" scoped>
.text-content {
  width: 100%;
  overflow: auto;
}
</style>
