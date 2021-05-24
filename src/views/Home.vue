<template>
  <div class="home">
    <BaseContainer>
      <template v-slot:header>
        <h1>Header</h1>
      </template>
      <p>The main content will go in here and it will keep going and going</p>
      <p>With more here</p>
      <template v-slot:footer>
        <span>Footer goes here</span>
      </template>
    </BaseContainer>
    <BaseButton to="/about"> </BaseButton>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseButton from '@/components/buttons/BaseButton.vue';
import BaseContainer from '@/components/containers/BaseContainer.vue';

export default defineComponent({
  name: 'Home',
  components: {
    BaseButton,
    BaseContainer,
  },
});
</script>

<style lang="scss" scoped>
.home {
  display: flex;
}
</style>
