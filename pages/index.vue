<template id = "index">
    <div id = "index_canvas">
        <div id = "index_header">
        <h1><b>Galaxy Raiders</b></h1>
        </div>
        <div id = "index_content">
          <router-link :to="{ path: '/game' }"><button class = "menubutton">Game</button></router-link>
          <router-link :to="{ path: '/leaderboard' }"><button class = "menubutton">Leaderboard</button></router-link>
          <router-link :to="{ path: '/close' }"><button class = "menubutton">Close</button></router-link>
        </div>
    </div>
</template>

<script>
    export default {
        onMounted() {
            window.onload = function() {
                if(!window.location.hash) {
                    window.location = window.location + '#loaded';
                    window.location.reload();
                }
            }
        }
    }
</script>

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
  left:430px;

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

  left:-15vw;
  font-size: 40px;
  color: #ffffff;
  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}

.menubutton {
  margin-right: 100px;
  width:200px;
  height:100px;

  font-size:20px;

  position: relative;

  background-color: #ffff00

}


</style>