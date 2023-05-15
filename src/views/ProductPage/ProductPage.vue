<template>
    <ion-page>
        <ion-content>
            <ion-card>
                <img alt="Silhouette of mountains" src="https://ionicframework.com/docs/img/demos/card-media.png" />
                <ion-card-header>
                    <ion-card-title>{{ $route.params.id }}</ion-card-title>
                    <ion-card-subtitle>Отличный выбор</ion-card-subtitle>
                </ion-card-header>

                <ion-card-content>
                    Here's a small text description for the card content. Nothing more, nothing less.
                </ion-card-content>
                <ion-card-content style="display: flex; align-items: center; justify-content: space-between;">
                    <ion-button fill="solid">В корзину</ion-button>
                    <p style="color: rgb(175 14 14);">Купить в 1 клик</p>
                </ion-card-content>
            </ion-card>
            <ion-card-content style="display: flex; align-items: center; color: #7ac900;">

                <ion-icon :icon="checkmarkCircleOutline"></ion-icon> Товар в наличии
            </ion-card-content>
            <ion-card-content style="display: flex; align-items: center;">
                <p>Артикул: 69420</p>
            </ion-card-content>
        </ion-content>
    </ion-page>
</template>
  
<script setup lang="ts">
import { IonPage, IonTitle, IonContent, IonToolbar, IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonRouterOutlet, IonRow, IonCol, IonCard, IonCardTitle, IonCardHeader, IonCardSubtitle, IonCardContent, IonButton } from '@ionic/vue';
import { ellipse, square, triangle, checkmarkCircleOutline } from 'ionicons/icons';

</script>
  