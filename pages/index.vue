<template>
    <div id="template">
        <div id="background">
            <div id="title">
                <img id="title" :src="titleImg" />
            </div>
            <div id="selection">
                <div class="indexbutton"><button><a href="game"><img class="indexbuttonImg" :src="startButton" /></a></button><img class="indexspaceship" :src="spaceship" /></div>
                <div class="indexbutton"><button><a href="leaderboard"><img class="indexbuttonImg" :src="scoreButton" /></a></button><img class="indexspaceship" :src="spaceship" /></div>
                <div class="indexbutton"><button><a href="https://www.google.com"><img class="indexbuttonImg" :src="exitButton" /></a></button><img class="indexspaceship" :src="spaceship" /></div>
            </div>

        </div>
    </div>
</template>

<script setup>
import titleImg from "assets/title.png"
import startButton from "assets/startButton.png"
import scoreButton from "assets/scoreButton.png"
import exitButton from "assets/exitButton.png"
import spaceship from "assets/spaceship.png"
</script>

<style>
#background{
    margin: 5%;
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}

body{
    background-image: url(assets/space.gif);
    background-repeat: no-repeat; 
    background-size: 100% 100%;
}
#template{
    display:flex;
    justify-content:center;
    background-image: url(assets/space.gif);
    background-repeat: no-repeat; 
    background-size: 100% 100%;
    width: 100%;
    height: 100%;
}

#title{
    width: 100%;
    margin-bottom: 5%;
}

#selection{
    display:flex;
    flex-direction: column;
    align-items: center;

}
.indexbutton{
    display: flex;
    flex-direction: row;
    width: auto;
    height: auto;
    justify-content: center;
    margin-bottom: 40%;
}

.indexbutton button{
    background-color: transparent;
    border-color: transparent;
    display: flex;
    align-items: center;
    
}

.indexbuttonImg{
    width: 100%;
    height: 50%;
}
.indexbutton button:hover ~ .indexspaceship{
    visibility: visible;
}

.indexspaceship{
    transform: rotate(-0.25turn);
    visibility: hidden;
    width: 30%;
 
}


</style>
