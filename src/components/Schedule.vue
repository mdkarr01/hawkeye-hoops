<template>
  <div>
    <table class="table table table-sm">
      <thead>
        <th class="header" colspan="7">2018-19 Iowa Hawkeye Basketball Schedule</th>
      </thead>
      <thead>
        <tr>
          <th scope="col">Date</th>
          <th scope="col">Time</th>
          <th scope="col">Opponent</th>
          <th scope="col">Location</th>
          <th scope="col">TV/Radio</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(game, index) in games" :key="game.index">
          <th scope="row">{{ game.date }}</th>
          <td>{{ game.time }}</td>
          <td>{{ game.opponent }}</td>
          <td>{{ game.location }}</td>
          <td>{{ game.details }}</td>
        </tr>
      </tbody>
    </table>

    <div></div>
  </div>
</template>

<script>
export default {
  props: ['games']
  // data() {
  //   return {
  //     players: []
  //   };
  // }
};
</script>

<style scoped>
div {
  border: 1px solid rgb(7, 0, 0);
  background-color: rgba(24, 2, 2, 0.8);
  padding: 10px;
  margin: 20px auto;
}

th {
  background-color: gold;
}

.header {
  font-size: 1.7em;
  background-color: rgba(24, 2, 2, 0.4);
  color: gold;
  border: none;
  font-style: italic;
}

td {
  color: white;
  padding: 5px 5px 5px 10px;
  font-size: 0.9em;
}
</style>
