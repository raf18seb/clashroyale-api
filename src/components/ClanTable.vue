<template>
  <div>
    <h2>Clan War Results</h2>
    <table>
      <thead>
        <tr>
          <th>Player</th>
          <th>Tag</th>
          <th>Średni wynik CW</th>
          <th>Wyniki na CW</th>
          <th>W ilu wojnach brali udział?</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="player in players" :key="player.tag">
          <td>{{ player.name }}</td>
          <td>{{ player.tag }}</td>
          <td>{{ player.averageFame }}</td>
          <td>{{ player.fameString }}</td>
          <td>{{ player.warsCount }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    players: {
      type: Array,
      required: true,
    },
  },
});
</script>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  padding: 8px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}
</style>
