<template>
    <div class="hello">
      <nav>
        <img src="https://cdn.7tv.app/emote/60b2b63c019c994a3a93f66c/2x.webp" alt="">
        <a href="#">Home</a>
      </nav>
    </div>
    <div class="data">
        <h3>Data from Json Server</h3>
        <div class="output"></div>
    </div>

  </template>
  
  <script>
  export default {
    
  }

      // Fetching Data from Json Server and adding it to HTML 
      async function jsData(){
        let data = await fetch("https://codi-k.github.io/json-server/games.Json")
        const stringGames =  await data.json()
        // console.log(stringGames);

        let info = stringGames.games
        // console.log(info);

        let result = document.querySelector(".output")

        info.forEach(data =>{
            result.innerHTML =`
            <img src="https://i.postimg.cc/sDJ6tqfP/ps4-god-of-war-ragnarok-launch-edition-box-front.webp" alt="God Of War">
            <h1>${data.game}</h1>
            <h2>Price : R 999 </h2>
            `

        })
    }

    jsData()
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style>
  nav{
    background-color: grey;
  
  }
  a{
    margin-left: 1rem ;
  }

  .data{
    padding: 1rem;
    text-align: center;
}
  
  </style>
  