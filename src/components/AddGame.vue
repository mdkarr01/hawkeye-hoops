<template>
    <div class="container">
      <form v-on:submit.prevent="addGame">
        <div class="row">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <h1>Add A Game</h1>
                <hr>
                <div class="form-group">
                    <label for="date">Date</label>
                    <input
                            type="text"
                            id="date"
                            class="form-control"
                            v-model.lazy="addDate">
                </div>

                <div class="form-group">
                    <label for="time">Time</label>
                    <input
                            type="text"
                            id="time"
                            class="form-control"
                            v-model.lazy="addTime">
                </div>

                <div class="form-group">
                    <label for="opponent">Opponent</label>
                    <input
                            type="text"
                            id="opponent"
                            class="form-control"
                            v-model="addOpponent">
                </div>

                <div class="form-group">
                    <label for="location">Location</label>
                    <input
                            type="text"
                            id="location"
                            class="form-control"
                            v-model="addLocation">
                </div>

                <div class="form-group">
                    <label for="details">Details</label>
                    <input
                        type="text"
                        id="details"
                        class="form-control"
                        v-model="addDetails">
                 </div>
            </div>
        </div>
      </form>
    </div>
</template>

<script>
export default {
  data() {
    return {
      addDate: '',
      addTime: '',
      addOpponent: '',
      addLocation: '',
      addDetail: ''
    }
    games: []
  },
  methods: {
    addGame() {
      this.games.push({
        date: this.addDate,
        time: this.addTime,
        opponent: this.addOpponent,
        location: this.addLocation,
        details: this.addDetails
      })
      this.addDate = '',
      this.addTime = '',
      this.addOpponent = '',
      this.addLocation = '',
      this.addDetails = ''
    }
  }
};
</script>

<style>
</style>


