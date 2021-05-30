<template>
  <div class="home">
    <HomeMainContent />
    <BaseLink :onClick="() => buttonClick('/about')">Base Link</BaseLink>
    <PrimaryButton title="Primary" :onClick="() => buttonClick('/about')" />
    <SecondaryButton title="Secondary" :onClick="() => buttonClick('/about')" />
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import HomeMainContent from './components/MainContent.vue';
import BaseLink from '@/components/buttons/BaseLink.vue';
import PrimaryButton from '@/components/buttons/PrimaryButton.vue';
import SecondaryButton from '@/components/buttons/SecondaryButton.vue';

export default defineComponent({
  name: 'Home',
  components: {
    HomeMainContent,
    PrimaryButton,
    SecondaryButton,
    BaseLink,
  },
  methods: {
    buttonClick(val: string) {
      return this.$router.push(val);
    },
  },
});
</script>

<style lang="scss" scoped></style>
