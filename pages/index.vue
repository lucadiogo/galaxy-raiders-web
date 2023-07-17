<template>
    <div id = canvas>
        <router-link :to="{ path: '/game' }"><button>Game</button></router-link>
        <router-link :to="{ path: '/leaderboard' }"><button>Leaderboard</button></router-link>
    </div>
</template>

<style>
#canvas {
  height: calc(100vh - 4rem);
  width: calc(100vw - 4rem);

  padding: 2rem;

  background-color: #4a1375;
  overflow: hidden;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>