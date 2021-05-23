<template>
  <div class="home">
    <BaseContainer>
      <p>The main content will go in here and it will keep going and going</p>
      <p>With more here</p>
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
