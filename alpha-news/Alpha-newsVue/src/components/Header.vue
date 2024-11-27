<script setup>
import { ref } from 'vue'

const count = ref(0)

function open () {
if (modalAppInfo.style.display == "block") {
    modalAppInfo.style.display = "none"
} else {modalAppInfo.style.display = "block"};
}

</script>

<template>

<header>
        <h1 id="logo">Alpha-News</h1>

        <nav>
            <a href="#" id="info" @click="open()">О нас</a>

            <section class="modalAppSection" id="modalAppInfo">
                <article id="modalAppInfo_text">
                    <h1>Alpha-News</h1>
                    <h2>Автомобильные новости</h2>
                        <section id="infoText">
                            <p>Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах. Российский союз автостраховщиков составил рейтинг популярных автомобилей Эксперты Российского союза страховщиков и Всероссийского союза страховщиков, изучили авторынок 
                                и составили рейтинг иномарок, которые пользуются спросом в Москве и регионах.</p>
                        </section>
                    

                </article>
             </section>

            <a href="">Наши партнеры</a>
            <a href="" id="LKbutton">Личный кабинет</a>

              <section id="accordeonReg">
                <dialog id="authDialogApp"></dialog>
                  <article id="accordeonRegContent">

                    <h1 id="regAccordeonH1">Регистрация</h1>

                    <p id="loginAuth" class="authDisplay">Ваш логин: #####</p>
                    <p id="emailAuth" class="authDisplay">Ваша почта: ####</p>
                    <button id="outAccount" class="authDisplay">Выйти</button>

                    <form name="regForm" id="regForm">
                        <dialog id="loginErrorEmpty"></dialog>
                        <input id="login" type="text" name="login" placeholder="Логин" minlength="4" maxlength="8">
                        <input type="text" name="password" placeholder="Пароль" minlength="6" maxlength="12">
                        <input type="text" name="forgotPassword" placeholder="Повторите пароль" minlength="6" maxlength="12">
                        <input type="text" name="email" placeholder="Введите почту" minlength="8" maxlength="40">
                        <input type="text" name="numberPhone" placeholder="Номер телефона" maxlength="12">
                        <button name="submit">Зарегестрироваться</button>
                        
                    </form>
                    
                    <form name="authForm" id="authForm">
                        <input id="login" type="text" name="login" placeholder="Логин" minlength="4" maxlength="8">
                        <input type="text" name="password" placeholder="Пароль" minlength="6" maxlength="12">
                        <button name="submit">Авторизоваться</button>
                    </form>
                    <button id="authButton">Уже есть аккаунт?</button>
                    
                  </article>
              </section>

        </nav>
    </header>
</template>

<style scoped>

header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    background-color: rgb(21, 21, 21);
}

a {
   text-decoration: none;
   padding-left: 10px;
   color: rgb(212, 212, 227);
   font-size: 18px;
}


#modalAppInfo {
    display: none;
}

#accordeonReg {
    display: none;
}

header {
    
}

#logo {
    color: #c0b844;
}

#modalAppInfo_text {
display: flex;
flex-direction: column;
text-align: center;
align-items: center;
}

#modalAppInfo_text > h1 {
    padding-top: 10px;
    font-size: 36px;

}

#modalAppInfo_text > h2 {
    font-size: 32px;
    font-weight: lighter;
}

#infoText {
    width: 70%;
    font-size: 24px;
    padding: 10px;
}

.modalAppSection {
    
    display: none;
    position: fixed;
    align-self: center;
    z-index: 1;
    width: 70%;
    height: 70%;
    background-color: rgba(218, 211, 211, 0.226);
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border-radius: 20px;
    overflow-y: scroll;
    border: 3px solid black;
}

.modalContent {
    text-align: center;
    display: none;
    width: 95%;
    height: 95%;
    align-items: center;
    padding: 20px 0px 100px 0px;
    flex-direction: column;

}

.modalContenAuthorAndDate {
    width: 70%;
    height: 5%;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333333;
}

.modalContenAuthorAndDate > article {
    padding: 15px;
}

.modalAppText {
    width: 70%;
    font-size: 24px;
    padding: 15px;
}

.modalAppText > h1 {
    font-size: 26px;
    padding-bottom: 10px;
}

.modalAppText > h2 {
    font-size: 24px;
    padding: 10px 20px;
    border-left: 5px solid darkred;
    color: darkred;
}

.modalContent > img{
    width: 70%;
    height: 60%;
}


</style>