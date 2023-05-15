<template>
    <ion-list>
        <ion-list-header>
            <ion-label style="font-size: 18px; font-weight: bold;">{{ name }}</ion-label>
        </ion-list-header>
        <IonItem v-for="item in catTypes">

            <a :href="'/sport_type/' + item.title" style="text-decoration: none;">
                <ion-card>
                    <img alt="Silhouette of mountains" :src="item.img"
                        style="height: 200px; width: 370px; background:cover;" />
                    <ion-card-header>
                        <ion-card-title>{{ item.title }}</ion-card-title>
                        <ion-card-subtitle></ion-card-subtitle>
                    </ion-card-header>

                    <ion-card-content>
                        {{ item.desc }}
                    </ion-card-content>
                </ion-card>
            </a>
        </IonItem>
    </ion-list>
</template>
  
  
<script setup lang="ts">
import { IonList, IonItem, IonListHeader, IonLabel, IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle } from '@ionic/vue';
let sportsType = ['Плавание', 'Кроссфит', 'Дзюдо', 'Водное поло'];

let catTypes = {
    item1: {
        title: 'Парфюм-боксы',
        desc: 'Удивите себя или своего близкого интересным набором парфюма',
        img: './parfume-box.jpg'
    },
    item2: {
        title: 'Для мужчин',
        desc: 'Подберите лучшие мужские ароматы азии',
        img: './parfume-for-men.jpg'
    },
    item3: {
        title: 'Для женщин',
        desc: 'Женщины-цветы жизни, и пахнуть с нашими духами будут изумительно!',
        img: './parfume-for-women.jpg'
    },
}

defineProps({
    name: String,
});
</script>
  
<style scoped></style>
  