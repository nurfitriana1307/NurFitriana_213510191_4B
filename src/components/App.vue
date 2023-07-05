<template>
  <div class="container">
    <h1>Semoga Harimu Menyenangkan :)</h1>
    <div class="card">
      <div class="card-item">
        <Cuaca/>
        <Lokasi/>
      </div>
    </div>
    <div class="card">
      <Stopwatch/>
    </div>
    <div class="card">
      <div class="card-item">
        <GameTicTacToe/>
        <GamePuzzle/>
      </div>
    </div>
    <div class="card">
      <Foto/>
    </div>
  </div>
</template>

<script>
import Cuaca from './Cuaca.vue';
import Lokasi from './Lokasi.vue';
import Stopwatch from './Stopwatch.vue';
import GameTicTacToe from './GameTicTacToe.vue';
import GamePuzzle from './GamePuzzle.vue';
import Foto from './Foto.vue';

export default {
  components: {
    Cuaca,
    Lokasi,
    Stopwatch,
    GameTicTacToe,
    GamePuzzle,
    Foto
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  margin-bottom: 20px;
  color: orchid;
}

.card-item {
  display: flex;
}

.card-item > * {
  flex: 1;
}
</style>
