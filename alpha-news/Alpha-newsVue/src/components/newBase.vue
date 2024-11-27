<script setup>
import { createElementBlock } from 'vue';


let props = defineProps({
  image: String,
  author: String,
  date: String,
  modalZag: String,
  modalText: String,
  type: String
})

function getImageUrl() {
  // This path must be correct for your file
  return new URL(`${props.image}`, import.meta.url)
}

let new_Url = getImageUrl().href
console.log(new_Url)

let image1 = "../assets/autoCraftImages/one.png"

</script>

<template>
<section class="newBase">
    <img id="mainImg" :src="new_Url" alt="">
    <span>
        <p class="nameNew">{{ type }}</p>
        <p class="date">{{ date }}</p>
    </span>
        <h3>В Киргизии откроют автозавод, машины которого могут привезти в Россию</h3>
        <h4>В Киргизии откроют автозавод, машины которого могут привезти в Россию</h4>

    <section class="modalAppSection">
        <article class="modalAppContent">
            <img :src="new_Url">
            <section class="authorAndDate">
                <p class="author">{{ author }}</p>
                <p class="date">{{ date }}</p>

                <section class="modalAppText">
                    <h1 class="zag">{{ modalZag }}</h1>
                    <p class="text">{{ modalText }}</p>

                </section>
            </section>
        </article>
    </section>


</section>
</template>

<style scoped>
.nameNew {
    font-weight: bold;
    background-color: #91705F;
    color: white;
    text-align: center;
    border-radius: 5px;
    padding: 2px 20px 2px 20px;
}

.newBase {
    width: 380px;
}

#mainImg {
    width: 380px;
}

.modalAppSection {
    display: none;
}
</style>