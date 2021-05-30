<template>
  <div class="home">
    <HomeMainContent />
    <BaseButton to="/about"> </BaseButton>
    <PrimaryButton title="Link" :onClick="() => buttonClick('/about')" />
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseButton from '@/components/buttons/BaseButton.vue';
import HomeMainContent from './components/MainContent.vue';
import PrimaryButton from '@/components/buttons/PrimaryButton.vue';

export default defineComponent({
  name: 'Home',
  components: {
    BaseButton,
    HomeMainContent,
    PrimaryButton,
  },
  methods: {
    buttonClick(val: string) {
      return this.$router.push(val);
    },
  },
});
</script>

<style lang="scss" scoped></style>
