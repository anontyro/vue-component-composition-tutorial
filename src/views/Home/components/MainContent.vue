<template>
  <div class="container-items">
    <BaseContainer>
      <template v-slot:header>
        <h1>Header</h1>
      </template>
      <div class="item-content">
        <p>The main content will go in here and it will keep going and going</p>
        <p>With more here</p>
      </div>
      <template v-slot:footer>
        <span>Footer goes here</span>
      </template>
    </BaseContainer>
    <ImageContainer
      imgName="mountain-lake.jpg"
      imgAlt="mountain with lake"
      classOverride="mountain-img"
    />
    <BaseContainer>
      <img
        class="img-item france-img"
        alt="looking out at Normady"
        src="@/assets/imgs/normandy-france.jpg"
      />
      <template v-slot:footer>
        <div class="footer-content">
          <span>A look out at Normandy France</span>
          <BaseButton to="/about">Take Me There</BaseButton>
        </div>
      </template>
    </BaseContainer>
    <InfoContainer title="Some Info will go here">
      <div>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus odio
        augue, eleifend ac elit at, laoreet consequat ex. Donec mattis, mauris
        vitae condimentum venenatis, sem est consequat metus, eget ultricies dui
        leo at eros. Proin semper dictum justo, at elementum sem fermentum vel.
        Aliquam dolor felis, venenatis nec magna sed, fringilla consectetur
        quam. Curabitur et ultrices arcu. Sed non mauris non nisl ultrices
        maximus. Donec eget fermentum odio. Vestibulum a justo odio. Sed
        vestibulum dolor ut leo condimentum, eget ornare sapien volutpat. Fusce
        sodales euismod metus, id euismod lorem scelerisque tempus. Cras posuere
        elit ut diam faucibus, nec ornare lectus finibus. Vestibulum
        sollicitudin lacus risus. Donec mauris diam, mattis in nisi in,
        consequat auctor urna. Vivamus eu varius orci. Fusce accumsan, purus
        quis tincidunt mollis, felis ligula feugiat massa, vitae gravida eros
        lacus a elit. Nam mollis molestie sollicitudin. Proin mollis sed sem
        quis luctus. Quisque justo diam, sagittis in risus sed, bibendum
        accumsan turpis. Fusce finibus sed velit ut aliquam. Nulla facilisi. Sed
        vulputate sagittis nisl, eu molestie libero mattis id. Ut consectetur
        porttitor nulla, id imperdiet nibh volutpat ut. Cras vel metus faucibus,
        porttitor lectus et, faucibus sem. Donec commodo tellus id feugiat
        maximus. Nulla eu tincidunt dolor. Mauris varius dapibus porttitor.
        Suspendisse vehicula ex at varius efficitur. Ut semper condimentum nunc.
        Maecenas gravida, est vehicula pulvinar blandit, ipsum est lacinia
        velit, ac feugiat odio urna eget mi. Cras ultrices, velit eu euismod
        dictum, lacus ipsum volutpat sapien, tristique pellentesque tortor ipsum
        sit amet ligula. Quisque tincidunt scelerisque neque, vel laoreet tellus
        tempor sed. Curabitur at arcu enim. Phasellus sagittis metus odio, et
        efficitur arcu semper eu. Aenean et neque vitae augue tincidunt feugiat.
        Praesent sollicitudin quam ac massa molestie, vitae tempor sapien
        faucibus. Donec efficitur, enim quis commodo suscipit, eros dolor
        ullamcorper dui, in sollicitudin urna risus quis leo. Ut semper egestas
        urna. Donec quis pharetra massa. Mauris eleifend maximus elit quis
        suscipit. Integer rhoncus libero vitae dolor egestas aliquam. Nunc nec
        dui magna. Fusce rhoncus nunc gravida ultricies tristique. Nunc ac
        vestibulum risus, in dignissim arcu. Suspendisse neque eros, maximus ac
        ante eu, blandit eleifend erat. Vivamus elit erat, venenatis quis lacus
        vitae, pulvinar hendrerit ligula. Praesent id tempor risus. Nulla a
        lacus in mi ornare lobortis at eget velit. Vivamus eu metus eu nulla
        tincidunt scelerisque sed sit amet est. Morbi quis libero vel mauris
        porta facilisis vitae et arcu. Maecenas fringilla eget ante in semper.
        Praesent vestibulum ipsum auctor, malesuada tortor vel, rhoncus odio.
        Fusce accumsan sodales magna et tempus. Sed venenatis massa vitae
        lobortis semper. Maecenas auctor lacinia velit quis hendrerit.
        Suspendisse rutrum quam sit amet enim pulvinar consequat. Duis molestie,
        dolor id commodo imperdiet, velit nisi porta risus, vel lacinia eros
        augue vulputate tortor. Praesent lobortis molestie imperdiet. Praesent
        pretium laoreet risus, eget dapibus justo finibus in.
      </div>
    </InfoContainer>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import BaseContainer from '@/components/containers/BaseContainer.vue';
import InfoContainer from '@/components/containers/InfoContainer.vue';
import ImageContainer from '@/components/containers/ImageContainer.vue';

export default defineComponent({
  name: 'HomeMainContent',
  components: {
    BaseContainer,
    InfoContainer,
    ImageContainer,
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
