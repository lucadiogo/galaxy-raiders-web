<template id = "index">
    <div id = "index_canvas">
        <div id = "index_header">
        <h1><b>Galaxy Raiders</b></h1>
        </div>
        <div id = "index_content">
          <router-link :to="{ path: '/game' }"><button>Game</button></router-link>
          <router-link :to="{ path: '/leaderboard' }"><button>Leaderboard</button></router-link>
        </div>
    </div>
</template>

<style>
#index_canvas {
  height: 100vh;
  width: 100vw;


  background-color: #4a1375;
  overflow: hidden;

  font-size: 40px;
  color: #ffffff;
  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}

#index_header{
  height: 100vh;

  padding:60px;

  background-color: #4a1375;
  overflow: hidden;

  font-size: 40px;
  color: #ffffff;
  position: relative;

  display: flex;
  text_align: center;
}

#index_content{
  background-color: #4a1375;
  overflow: hidden;

  left:-20vw;
  font-size: 40px;
  color: #ffffff;
  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}


</style>