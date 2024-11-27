<script setup>

</script>

<template>


<section id="glavnaya">

    <video autoplay muted class="bgvideo" id="bgvideo">
        <source src="../assets/videoBG.mp4" type="video/mp4"></source>
       </video>

         <article id="zagolovokInGlavnaya">
             <h1 class="">Самые свежие новости из автомобильного мира <b class="cssanimation leFadeIn sequence">ТОЛЬКО У НАС!</b></h1>
             <button class="buttonTrueBackground">Продвижение</button>
             <button class="buttonFalseBackground">Новости</button>
         </article>

         <article id="navOnBlocks">
           <span id="rdsNavButton" class="navBlockBase"><a href="#autoCraftSection">Новости RDS</a></span>
           <span id="f1NavButton" class="navBlockBase"><a href="#f1Section">Новости F1</a></span>
           <span id="autocraftNavButton" class="navBlockBase"><a href="#">Новости машиностроения</a></span>
           <span id="actionsNavButton" class="navBlockBase"><a href="#">События</a></span>
         </article>
    </section>

<section class="blackLine"></section>
</template>

<style scoped>
#glavnaya {
    display: grid;
    grid-template-columns: 1fr 1fr;
    background-color: black;
    padding: 0px 100px 0px 100px;
    background: url('../assets/videoBG.png');
    background-size: cover;
    background-repeat: no-repeat;
}

.bgvideo {
    position: absolute;
    right: 0;
    bottom: 0;
    top: 0;
    width: 100%;
    height: auto;
    z-index:-1;
  }

#zagolovokInGlavnaya {
display: flex;
flex-direction: column;
justify-content: center;
}

#navOnBlocks {
    display: flex;
    flex-direction: column;
    align-items: end;
    justify-content: center;
    padding: 20px;
    gap: 20px;
}
#navOnBlocks > span > a {
    text-decoration: none;
    color: white;
}
#navOnBlocks > span {
    width: 350px;
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
}

#zagolovokInGlavnaya > h1 {
    font-size: 46px;
    width: 540px;
    padding: 20px;
    color: white;
}

#zagolovokInGlavnaya > button {
    margin-left: 20px;
}

#zagolovokInGlavnaya > button:not(.buttonTrueBackground) {
    margin-left: 20px;
    margin-top: 10px;
}

/* Навигация по блокам страницы */

.navBlockBase {
    color: white;
    font-size: 28px;
    font-weight: bold;
    border: 3px solid #91705F;
    border-radius: 5px;
    text-align: center;
}

#rdsNavButton {
    background-image: url(../assets/RdsNavBackground.png);
}

#f1NavButton {
    background-image: url(../assets/F1NavBackground.png);
}

#autocraftNavButton {
    background-image: url(../assets/AutoCraftNavBackground.png);
}

#actionsNavButton {
    background-image: url(../assets/ActionsBackground.png);
}

</style>