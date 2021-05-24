<template>
  <BaseContainer>
    <img
      :class="`img-item ${classOverride}`"
      :alt="imgAlt"
      :src="require(`@/assets/imgs/${imgName}`)"
    />
  </BaseContainer>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseContainer from './BaseContainer.vue';

export default defineComponent({
  name: 'ImageContainer',
  components: {
    BaseContainer,
  },
  props: {
    imgName: String,
    imgAlt: {
      type: String,
      default: 'Some beautiful image most likely',
    },
    classOverride: String,
  },
});
</script>

<style lang="scss" scoped>
.img-item {
  width: 100%;
}
</style>
