<template>
    <div>
        <div v-for="data in myJson">{{data}}</div>
    </div>
</template>


<script>
      import json from '../../galaxy-raiders-api/app/core/score/Leaderboard.json'
      export default{
          data(){
              return{
                  myJson: json
              }
          }
      }
</script>

