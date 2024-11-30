<script setup>
import { createElementBlock } from 'vue';

import { ref } from 'vue';

let okay = ref(false)



let props = defineProps({
  image: String,
  author: String,
  date: String,
  zag: String,
  podzag: String,
  modalText: String,
  type: String
})

function getImageUrl() {
  return new URL(`${props.image}`, import.meta.url)
}

let new_Url = getImageUrl().href

</script>

<template>
<section @:click="okay = !okay" class="newBase">
    <img id="mainImg" :src="new_Url" alt="">
    <span>
        <p class="type">{{ type }}</p>
        <p class="date">{{ date }}</p>
    </span>
        <h3>{{ zag }}</h3>
        <h4>{{ podzag }}</h4>
    
        <section id="modalAppSection" v-show="okay">
            <article id="modalContent">
                <img :src="new_Url" alt="">
                <section id="modalContenAuthorAndDate">
                    <article><p>{{ author }}, {{ date }}</p></article>
                    <article><p>Alpha-News</p></article>
                </section>

                <section id="modalAppText">
                    <h1>{{ zag }}</h1>
                    <h2>{{ podzag }}</h2>
                    <p>{{ modalText }}</p>
                </section>

            </article>
         </section>
    

</section>
</template>

<style scoped>
#modalAppSection {
    display: flex;
    position: fixed;
    align-self: center;
    z-index: 1;
    width: 95%;
    height: 95%;
    background-color: rgb(252, 252, 252);
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border-radius: 20px;
    overflow-y: scroll;
    border: 3px solid black;
}

#modalContent {
    display: flex;
    width: 95%;
    height: 95%;
    align-items: center;
    padding: 20px 0px 100px 0px;
    flex-direction: column;

}

#modalContenAuthorAndDate {
    width: 70%;
    height: 5%;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333333;
}

#modalContenAuthorAndDate > article {
    padding: 15px;
}

#modalAppText {
    width: 70%;
    font-size: 24px;
    padding: 15px;
}

#modalAppText > h1 {
    font-size: 26px;
    padding-bottom: 10px;
}

#modalAppText > h2 {
    font-size: 24px;
    padding: 10px 20px;
    border-left: 5px solid darkred;
    color: darkred;
}

#modalContent > img{
    width: 70%;
    height: 60%;
}





span {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 10px;
}
.type {
    font-weight: bold;
    background-color: #91705F;
    color: white;
    text-align: center;
    border-radius: 5px;
    padding: 2px 20px 2px 20px;
}
.newBase {
    width: 450px;
    height: 400px;
    background-color: white;
}

#mainImg {
    width: 450px;
    height: 250px;
}

h3 {
    padding: 0px 10px;
    padding-bottom: 5px;
}

h4 {
font-weight: normal;
opacity: 50%;
padding: 0px 10px;
padding-bottom: 10px;
}
</style>