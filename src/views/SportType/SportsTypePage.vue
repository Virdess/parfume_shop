<template>
    <ion-page>
        <ion-content>
            <ion-toolbar>
                <ion-title>
                    {{ $route.params.id }}
                </ion-title>
            </ion-toolbar>
            <ion-toolbar>
                <ion-tabs>
                    <ion-router-outlet></ion-router-outlet>
                    <ion-tab-bar slot="bottom">
                        <ion-tab-button tab="tab1">
                            <ion-label>Сегодня</ion-label>
                        </ion-tab-button>

                        <ion-tab-button tab="tab2">
                            <ion-label>На этой неделе</ion-label>
                        </ion-tab-button>

                        <ion-tab-button tab="tab3">
                            <ion-label>В этом месяце</ion-label>
                        </ion-tab-button>
                    </ion-tab-bar>
                </ion-tabs>
            </ion-toolbar>
            <IonCard v-for="item in today" style="width: 95%;">
                <IonCardHeader>
                    <IonCardTitle>
                        {{ item.title }}
                    </IonCardTitle>
                    <ion-card-subtitle>
                        {{ item.time }}
                    </ion-card-subtitle>
                </IonCardHeader>
                <IonCardContent>
                    {{ item.where }}
                </IonCardContent>
            </IonCard>
            <IonRow>
                <IonRow style="width: 100%; margin: 0;">
                    <IonCol style="width: max-content;">
                        <h4></h4>
                    </IonCol>
                    <IonCol>
                        <p></p>
                    </IonCol>
                </IonRow>
                <IonRow style="width: 100%;">
                    <p></p>
                </IonRow>
            </IonRow>
        </ion-content>
    </ion-page>
</template>
  
<script setup lang="ts">
import { IonPage, IonTitle, IonContent, IonToolbar, IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonRouterOutlet, IonRow, IonCol, IonCard, IonCardTitle, IonCardHeader, IonCardSubtitle, IonCardContent } from '@ionic/vue';
import { ellipse, square, triangle } from 'ionicons/icons';

let today = {
    item1: {
        title: 'Тренировки с тренером',
        time: '22:00-23:00',
        where: 'Астана, ДС "Жастар"'
    },
    item2: {
        title: 'Тренировка в зале',
        time: '12:00-14:30',
        where: 'Aray фитнесс центр для мужчин'
    },
    item3: {
        title: 'Самостоятельные занятия',
        time: '20:40-22:20',
        where: 'Sport city'
    },
    item4: {
        title: 'Тренировки с тренером',
        time: '12:00-14:30',
        where: 'Koktal Zal'
    },
}
</script>
  