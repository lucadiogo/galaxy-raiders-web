<template id = "leader">
    <div id ="lb_canvas">
        <div id="lb_header">
            <h1><b>Leaderboard</b></h1>
        </div>
        <div id = "lb_content">    
            <table>
                <thead>
                    <tr>
                        <th scope="col">Score</th>
                        <th scope="col">Asteroids</th>
                        <th scope="col">Date</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="i in info">
                        <td>{{i[0]}}</td>
                        <td>{{i[1]}}</td>
                        <td>{{i[2]}}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>


<script>
    import json from '../../galaxy-raiders-api/app/core/score/Leaderboard.json'
    export default {
        data() {
            return {
                info: json.map(data => [data.score, data.asteroidsDestroyed, data.date]),
            }
        }
    }
</script>

<style>
  td {
    padding: 0 35px;
  }


#lb_canvas {
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

#lb_header{
  height: 100vh;

  padding:60px;
  left:400px;

  background-color: #4a1375;
  overflow: hidden;

  font-size: 40px;
  color: #ffffff;
  position: relative;

  display: flex;
  text_align: center;
}

#lb_content{
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

