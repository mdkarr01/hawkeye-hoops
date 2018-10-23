<template>
  <div>
    <table class="table table table-sm">
      <thead>
        <th class="header" colspan="7">2018-19 Iowa Hawkeye Basketball Roster</th>
      </thead>
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Name</th>
          <th scope="col">Pos</th>
          <th scope="col">Height</th>
          <th scope="col">Weight</th>
          <th scope="col">Year</th>
          <th scope="col">High School/Hometown</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="player in players">
          <th scope="row">{{ player.number }}</th>
          <td>{{ player.name }}</td>
          <td>{{ player.position }}</td>
          <td>{{ player.height }}</td>
          <td>{{ player.weight }}</td>
          <td>{{ player.year }}</td>
          <td>{{ player.highschool }}/{{ player.hometown }}</td>
        </tr>
      </tbody>
    </table>

    <div></div>

    <table style="width: 50%; margin-bottom: 10em; text-align: left;" class="table">
      <thead>
        <th class="header" colspan="7">Coaching Staff</th>
      </thead>
      <thead>
        <tr>
          <th scope="col">Name</th>
          <th scope="col">Position</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="coach in coaches">
          <td>{{ coach.name }}</td>
          <td>{{ coach.position }}</td>
        </tr>
      </tbody>
    </table>    <!-- <ul>
      <li v-for='player in players'>{{player.name}} {{player.weight}}</li>
    </ul> -->
  </div>
</template>

<script>
export default {
  props: ['players', 'coaches']
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
  /* text-align: center; */
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

