<template>
  <InfoContainer title="Test Form">
    <div class="main-container">
      <div class="main-form" v-if="!state.isPreview">
        <div class="form-field">
          <label for="" class="">First Name:</label>
          <input v-model="state.firstName" placeholder="First Name" />
        </div>
        <div class="form-field">
          <label for="" class="">Last Name:</label>
          <input v-model="state.lastName" placeholder="Last Name" />
        </div>
        <div class="form-field">
          <label for="" class="">UserName:</label>
          <input v-model="state.userName" placeholder="UserName" />
        </div>
      </div>
      <div class="form-preview" v-if="state.isPreview">
        <div class="form-field">
          <label>First Name:</label>
          <span>{{ state.firstName }}</span>
        </div>
        <div class="form-field">
          <label>Last name:</label>
          <span>{{ state.lastName }}</span>
        </div>
        <div class="form-field">
          <label>UserName:</label>
          <span>{{ state.userName }}</span>
        </div>
      </div>
      <div class="button-container">
        <SecondaryButton
          :title="state.isPreview ? 'Form' : 'Preview'"
          @click="togglePreview"
        />
        <PrimaryButton title="Submit Form" @click="submitForm" />
      </div>
    </div>
  </InfoContainer>
</template>
<script lang="ts">
import Vue, {defineComponent, reactive} from 'vue';
import InfoContainer from '../containers/InfoContainer.vue';
import PrimaryButton from '../buttons/PrimaryButton.vue';
import SecondaryButton from '../buttons/SecondaryButton.vue';

export default defineComponent({
  name: 'MainForm',
  components: {
    InfoContainer,
    PrimaryButton,
    SecondaryButton,
  },
  setup() {
    const state = reactive({
      firstName: '',
      lastName: '',
      userName: '',
      isPreview: false,
    });
    return {state};
  },
  methods: {
    togglePreview() {
      this.state.isPreview = !this.state.isPreview;
      return this.state.isPreview;
    },
    submitForm() {
      console.log('submit pressed');
    },
  },
});
</script>

<style lang="scss" scoped>
.main-container {
  display: flex;
  flex-direction: column;
}
.button-container {
  display: flex;
  justify-content: center;
}

.main-form {
  display: flex;
  flex-direction: column;
  width: 75%;
  margin: auto;
  padding: 10px;
}
.form-field {
  display: flex;
  justify-content: space-evenly;
  margin: 10px 0;
}
</style>
