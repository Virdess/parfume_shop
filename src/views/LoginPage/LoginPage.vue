<template>
    <ion-page style="text-align: center;">
        <ion-list>
            <ion-card style="text-align: center;">
                <ion-card-header>
                    <ion-card-title>Добро пожаловать!</ion-card-title>
                    <ion-card-subtitle>Онлайн абонемент</ion-card-subtitle>
                </ion-card-header>

                <ion-card-content>
                    Это приложение поможет вам не париться насчёт того, взяли ли вы свой абонемент с собой, ведь он всегда с
                    вами в вашем телефоне! {{ someshit }}
                </ion-card-content>
            </ion-card>
            <ion-item>
                <ion-input label="Логин" placeholder="Введите логин"></ion-input>
            </ion-item>
            <ion-item>
                <ion-input label="Пароль" type="password" placeholder="password"></ion-input>
            </ion-item>
            <ion-button color="success" style="margin: 30px;" href="/tabs">Next</ion-button>
        </ion-list>
    </ion-page>
</template>
  
<script setup lang="ts">
import { IonPage, IonInput, IonItem, IonList, IonCard, IonCardContent, IonCardHeader, IonCardTitle, IonCardSubtitle, IonHeader, IonButton } from '@ionic/vue';
import axios from 'axios'
import { Ref, ref } from 'vue';
let someshit: any = ref("")

axios.post('http://192.168.1.5:4444/auth/reg',
    {
        email: "asdasd@asd.as",
        userName: "asd",
        password: "123456"
    }
)
    .then(function (response) {
        console.log(response);
    })
    .catch(function (error) {
        console.log(error);
    });
</script>
  