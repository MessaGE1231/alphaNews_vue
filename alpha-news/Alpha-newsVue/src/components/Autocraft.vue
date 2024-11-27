<script setup>
import newBase from './newBase.vue';
</script>

<template>
<section id="allSection">

    <h1>Автомобилестроение</h1>



    <section id="autoCraftSection">
        <article class="new"><newBase image="../assets/autoCraftImages/one.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/one.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
        <article class="new"><newBase image="../assets/autoCraftImages/two.png" author="Максим Костив" date="23 марта 2024 года" modalZag="Хуйня" modalText="Хуйня2вфывфы" type="Автомобилестроение"/></article>
    </section>

</section>
</template>

<style scoped>
h1 {
    font-size: 32px;
}

#allSection {
    display: flex;
    background-color: white;
    flex-direction: column;
    align-items: center;
}

#autoCraftSection {
    background-color: white;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
   }

.new {
    padding-top: 30px;
    padding: 20px;
}
</style>