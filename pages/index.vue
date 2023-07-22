<template>
    <div id="template">
        <div id="background">
            <div id="title">
                <img id="title" :src="titleImg" />
            </div>
            <div id="selection">
                <div><button class="indexbutton"><a href="game"><img class="indexbuttonImg" :src="startButton" /></a></button><img class="indexspaceship" :src="spaceship" /></div>
                <div><button class="indexbutton"><a href="leaderboard"><img class="indexbuttonImg" :src="scoreButton" /></a></button><img class="indexspaceship" :src="spaceship" /></div>
                <div><button class="indexbutton"><a href="http://www.google.com"><img class="indexbuttonImg" :src="exitButton" /></a></button><img class="indexspaceship" :src="spaceship" /></div>
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
    margin: 15em;
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}

#template{
    display:flex;
    justify-content:center;
    background-image: url(assets/space.gif);
    background-repeat: no-repeat; 
    background-size: 100vw 100vh;
    width: 100vw;
    height: 100vh;
}

#title{
    width: 200em;
}

#selection{
    display:flex;
    flex-direction: column;
}
.indexbutton{
    background-color: transparent;
    width: 25em;
    height: 8em;
    border-color: transparent;
    margin-top: 10em;
}

.indexbuttonImg{
    width: 25em;
    height: 8em;
}
.indexbutton:hover ~ .spaceship{
    visibility: visible;

}
.indexspaceship{
    transform: rotate(-0.25turn);
    visibility: hidden;
    width: 10em;

    
}


</style>
