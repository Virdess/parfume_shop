<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>QR</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>
      <StreamBarcodeReader @decode="onDecode" @loaded="onLoaded"></StreamBarcodeReader>
      <ion-alert :is-open="isOpen" header="Успешно" message="Успешно отсканировано. Ожидайте ответа от сервера"
        :buttons="alertButtons" @didDismiss="setOpen(false)"></ion-alert>
      <ExploreContainer name="Tab 2 page" />
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">

import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonAlert, IonButton, alertController } from '@ionic/vue';
import { StreamBarcodeReader } from "vue-barcode-reader";
import ExploreContainer from '@/components/ExploreContainer.vue';

import { ref } from "vue";

const decodedText = ref("");
let isOpen = ref(false);
const alertButtons = ['OK'];

const onLoaded = () => {
  console.log("loaded");
};

const onDecode = (text: any) => {
  setOpen(true)
  console.log(decodedText)
  decodedText.value = text;
};
const setOpen = (bool: boolean) => {
  isOpen.value = bool;
}
</script>
