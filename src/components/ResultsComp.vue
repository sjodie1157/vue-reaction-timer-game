<template>
    <p>Reaction time - {{ score }}</p>
    <p class="speed">{{ speed }}</p>
  </template>
  
  <script>
  export default {
      props: ['score'],
      data() {
          return {
              speed: null
          }
      },
      mounted() {
        if(this.score < 250) {
            this.speed = "Very fast"
        }
        else if (this.score < 400 ) {
          this.speed = "Relatively fast"  
        }  
        else {
          this.speed = "Not so fast"
        }
      }
  }
  </script>
  
  <style>
    .speed {
        font-size: 1.4em;
        color:forestgreen;
        font-weight: bold;
    }
  </style>