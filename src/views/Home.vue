<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Login</ion-title>
        <ion-button
          href="/native"
          fill="clear"
        >Native</ion-button>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <h1>Don't put real passwords here</h1>

      <ion-item>
        <ion-input
          placeholder="Username"
          autocomplete="username"
          :autofocus="true"
          v-model="username"
          @ion-input="inputTrigger"
          @ion-change="changeTrigger"
          @ion-blur="blurTrigger"
        ></ion-input>
      </ion-item>

      <ion-item>
        <ion-input
          placeholder="Password"
          type="password"
          autocomplete="current-password"
          v-model="password"
        ></ion-input>
      </ion-item>

      <ion-button
        type="submit"
        expand="block"
      >Submit</ion-button>

      <ion-item><p>{{ username }}</p></ion-item>
      <ion-item><p>{{ password }}</p></ion-item>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonButton, IonContent, IonHeader, IonInput, IonItem, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Login',

  components: {
    IonButton,
    IonContent,
    IonHeader,
    IonInput,
    IonItem,
    IonPage,
    IonTitle,
    IonToolbar
  },

  data() {
    return {
      username: null,
      password: null
    };
  },

  methods: {
    inputTrigger() {
      console.log('inputTrigger');
    },
    changeTrigger() {
      console.log('changeTrigger');
    },
    blurTrigger() {
      console.log('blurTrigger');
    }
  }
});
</script>
