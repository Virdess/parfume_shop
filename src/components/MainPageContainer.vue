<template>
    <ion-list>
        <ion-list-header>
            <ion-label style="font-size: 18px; font-weight: bold;">{{ name }}</ion-label>
        </ion-list-header>
        <IonItem v-for="item in sportsType" :key="item">
            <ion-label>
                <a :href="'/sport_type/' + item" style="text-decoration: none;">
                    {{ item }}
                </a>
            </ion-label>
        </IonItem>
    </ion-list>
</template>
  
  
<script setup lang="ts">
import { IonList, IonItem, IonListHeader, IonLabel } from '@ionic/vue';
let sportsType = ['Плавание', 'Кроссфит', 'Дзюдо', 'Водное поло'];
let sportsTypeCount: any;
for (let index = 0; index < sportsType.length; index++) {
    sportsTypeCount = index + 1

}
defineProps({
    name: String,
});
</script>
  
<style scoped></style>
  