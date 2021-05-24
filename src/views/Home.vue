<template>
  <div class="home">
    <div class="container-items">
      <BaseContainer>
        <template v-slot:header>
          <h1>Header</h1>
        </template>
        <div class="item-content">
          <p>
            The main content will go in here and it will keep going and going
          </p>
          <p>With more here</p>
        </div>
        <template v-slot:footer>
          <span>Footer goes here</span>
        </template>
      </BaseContainer>
      <BaseContainer>
        <img
          class="img-item mountain-img"
          alt="mountain with lake"
          src="../assets/imgs/mountain-lake.jpg"
        />
      </BaseContainer>
      <BaseContainer>
        <img
          class="img-item france-img"
          alt="looking out at Normady"
          src="../assets/imgs/normandy-france.jpg"
        />
        <template v-slot:footer>
          <div class="footer-content">
            <span>A look out at Normandy France</span>
            <BaseButton to="/about">Take Me There</BaseButton>
          </div>
        </template>
      </BaseContainer>
    </div>
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
.container-items {
  display: flex;
  flex-wrap: wrap;
}
.img-item {
  width: 100%;
}
.footer-content {
  display: flex;
  flex-direction: column;
}
</style>
