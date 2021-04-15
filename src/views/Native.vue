<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Native</ion-title>
        <ion-button
          href="/home"
          fill="clear"
        >Home</ion-button>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <h1>Don't put real passwords here</h1>

      <ion-item>
        <input
          placeholder="Username"
          autocomplete="username"
          :autofocus="true"
          v-model="username"
          @input="inputTrigger"
          @change="changeTrigger"
          @blur="blurTrigger"
        />
      </ion-item>

      <ion-item>
        <input
          placeholder="Password"
          type="password"
          autocomplete="current-password"
          v-model="password"
        />
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
import { IonButton, IonContent, IonHeader, IonItem, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Native',

  components: {
    IonButton,
    IonContent,
    IonHeader,
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
