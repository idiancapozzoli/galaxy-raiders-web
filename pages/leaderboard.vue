<template>
    <div id="board">
        <div id="title">
            <img id="title-leaderboard" :src="titleImg" />
        </div>
        <h1>Leaderboard</h1>
        <table>
          <thead>
            <tr>
              <th>Date & time</th>
              <th>Destroyed asteroids</th>
              <th>Score</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(data, datetime) in board" :key="datetime">
                <td>{{ formatDateTime(datetime) }}</td>
                <td>{{ data.destroyedAsteroids }}</td>
                <td>{{ data.score }}</td>
            </tr>
          </tbody>
        </table>
    </div>
  </template>
  
  <script setup>
    import titleImg from "assets/title.png"
    </script>

  <script>
  import JSON from '~/score/Leaderboard.json'
  
  export default {
    data() {
        return {
        board: JSON,
        };
    },
    methods: {
        formatDateTime(datetime) {
        return new Date(datetime).toLocaleString();
        },
    },
  };
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Sarpanch:wght@500&display=swap');
  
  #title-leaderboard{
    width: 60%;
    margin-top: 3%;
    margin-bottom: 4%;
}

  #board {
    height: calc(100% - 10rem);
    width: calc(100% - 10rem);
    
    color: orange;
    font-family: 'Sarpanch';
    font-size: large;
  
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  
  </style>