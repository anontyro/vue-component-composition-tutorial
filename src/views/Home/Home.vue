<template>
  <div class="home">
    <HomeMainContent />
    <BaseButton to="/about"> </BaseButton>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseButton from '@/components/buttons/BaseButton.vue';
import HomeMainContent from './components/MainContent.vue';

export default defineComponent({
  name: 'Home',
  components: {
    BaseButton,
    HomeMainContent,
  },
});
</script>

<style lang="scss" scoped></style>
