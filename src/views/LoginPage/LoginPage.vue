<template>
    <ion-page style="text-align: center;">
        <ion-list>
            <ion-card style="text-align: center;">
                <ion-card-header>
                    <ion-card-title>Добро пожаловать!</ion-card-title>
                    <ion-card-subtitle>PoDARI</ion-card-subtitle>
                </ion-card-header>

                <ion-card-content>
                    Вы попали в самый лучший онлайн-магазин парфюмерии в интернете! Просим к столу:{{ someshit }}
                </ion-card-content>
            </ion-card>
            <ion-item>
                <ion-input label="Логин" placeholder="Введите логин"></ion-input>
            </ion-item>
            <ion-item>
                <ion-input label="Пароль" type="password" placeholder="Пароль"></ion-input>
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
  