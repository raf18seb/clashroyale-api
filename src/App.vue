<!-- <template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style> -->

<template>
  <div id="app">
    <ClanTable :players="players" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ClanTable from './components/ClanTable.vue';

export default defineComponent({
  components: {
    ClanTable,
  },
  data() {
    return {
      players: [
        {
          name: 'Player 1',
          tag: 'ABC123',
          averageFame: 2500,
          fameString: '2500 + 2600 + 2700',
          warsCount: 10,
        },
        {
          name: 'Player 2',
          tag: 'ABC124',
          averageFame: 2700,
          fameString: '2500 + 2600 + 3700',
          warsCount: 8,
        },
      ],
    };
  },
});
</script>
