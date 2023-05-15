<template>
    <ion-page>
        <product-component></product-component>
    </ion-page>
</template>
  
<script setup lang="ts">
import { IonPage, IonTitle, IonContent, IonToolbar, IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonRouterOutlet, IonRow, IonCol, IonCard, IonCardTitle, IonCardHeader, IonCardSubtitle, IonCardContent, IonButton } from '@ionic/vue';
import { ellipse, square, triangle, checkmarkCircleOutline } from 'ionicons/icons';
import ProductComponent from '@/components/ProductComponent.vue';
</script>
  