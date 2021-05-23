<template>
  <div class="home">
    <BaseButton to="/about"> </BaseButton>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseButton from '@/components/buttons/BaseButton.vue';

export default defineComponent({
  name: 'Home',
  components: {
    BaseButton,
  },
});
</script>
