<script setup lang="ts">
import { TheChessboard, type BoardApi, type BoardConfig } from '@/index';
import '@/assets/board.css';

let boardAPI: BoardApi | undefined;

const boardConfig: BoardConfig = {
  coordinates: true,
  autoCastle: false,
};
const playerColor: 'white' | 'black' | 'both' | undefined = undefined;
</script>

<template>
  <TheChessboard
    :board-config="boardConfig"
    :player-color="playerColor"
    @board-created="(api) => (boardAPI = api)"
  />
</template>

<style>
body {
  background-color: #222;
}
</style>
