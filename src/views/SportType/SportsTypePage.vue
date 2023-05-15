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
                            <ion-label>Самое популярное</ion-label>
                        </ion-tab-button>

                        <ion-tab-button tab="tab2">
                            <ion-label>Самое дешёвое</ion-label>
                        </ion-tab-button>

                        <ion-tab-button tab="tab3">
                            <ion-label>Новинки сезона</ion-label>
                        </ion-tab-button>
                    </ion-tab-bar>
                </ion-tabs>
            </ion-toolbar>
            <IonCard v-if="$route.params.id == 'Парфюм-боксы'" v-for="item in boxes" style="width: 95%;">
                <RouterLink :to="'/product/' + item.title" style="text-decoration: none !important;">
                    <IonCardHeader>
                        <IonCardTitle>
                            {{ item.title }}
                        </IonCardTitle>
                        <ion-card-subtitle>
                            {{ item.price }} тг.
                        </ion-card-subtitle>
                    </IonCardHeader>
                    <IonCardContent>
                        {{ item.where }}
                    </IonCardContent>
                </RouterLink>
            </IonCard>
            <IonCard v-else-if="$route.params.id == 'Для мужчин'" v-for="item in men" style="width: 95%;">
                <RouterLink :to="'/product/' + item.title" style="text-decoration: none !important;">
                    <IonCardHeader>
                        <IonCardTitle>
                            {{ item.title }}
                        </IonCardTitle>
                        <ion-card-subtitle>
                            {{ item.price }} тг.
                        </ion-card-subtitle>
                    </IonCardHeader>
                    <IonCardContent>
                        {{ item.where }}
                    </IonCardContent>
                </RouterLink>
            </IonCard>
            <IonCard v-else="$route.params.id == 'Для мужчин'" v-for="item in women" style="width: 95%;">
                <RouterLink :to="'/product/' + item.title" style="text-decoration: none !important;">
                    <IonCardHeader>
                        <IonCardTitle>
                            {{ item.title }}
                        </IonCardTitle>
                        <ion-card-subtitle>
                            {{ item.price }} тг.
                        </ion-card-subtitle>
                    </IonCardHeader>
                    <IonCardContent>
                        {{ item.where }}
                    </IonCardContent>
                </RouterLink>
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

let boxes = {
    item1: {
        title: 'Подарочный бокс для девушки',
        price: 8990,
        where: ''
    },
    item2: {
        title: 'Подарочный бокс для парня',
        price: 15400,
        where: ''
    },
    item3: {
        title: 'Бокс "Весна"',
        price: 12000,
        where: ''
    },
    item4: {
        title: 'Бокс "Финляндия"',
        price: 4650,
        where: ''
    },
}

let men = {
    item1: {
        title: 'Мужской адеколон "Горбатая свежесть"',
        price: 8990,
        where: ''
    },
    item2: {
        title: 'Мужской адеколон пот горного льва',
        price: 15400,
        where: ''
    },
    item3: {
        title: 'Мужской адеколон со льдами арктики',
        price: 12000,
        where: ''
    },
    item4: {
        title: 'Мужской адеколон "Сила угля с углём"',
        price: 4650,
        where: ''
    },
}

let women = {
    item1: {
        title: 'Запах розовой лаванды',
        price: 8990,
        where: ''
    },
    item2: {
        title: 'Весенняя нежность пера',
        price: 15400,
        where: ''
    },
    item3: {
        title: 'Летняя апельсиновая корка',
        price: 12000,
        where: ''
    },
    item4: {
        title: 'Розы и леса японии',
        price: 4650,
        where: ''
    },
}
</script>
  