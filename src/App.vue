<template>
  <div class="container">
    <div class="links">
      <h3 @click="selectedComponent='appSchedule'">Schedule</h3>
      <h3 @click="selectedComponent='appRoster'">Roster</h3>
    </div>

<transition name="fade" mode="out-in">
   <component :players="players" :coaches="coaches" :games="games" :is="selectedComponent">
        <p>This is content</p>
   </component>
  </transition>
  </div>
</template>

<script>
import Roster from './components/Roster.vue';
import Schedule from './components/Schedule.vue';
export default {
  components: {
    appRoster: Roster,
    appSchedule: Schedule
  },

  data() {
    return {
      selectedComponent: '',
      players: [
        {
          number: 0,
          name: 'Michael Baer',
          height: "6'6",
          weight: 200,
          year: 'Sr',
          position: 'F',
          highschool: 'Bettendorf HS',
          hometown: 'Bettendorf, IA'
        },

        {
          number: 1,
          name: 'Maishe Dailey',
          height: "6'7",
          weight: 200,
          year: 'Jr',
          position: 'G',
          highschool: 'Beachwood',
          hometown: 'Beachwood, OH'
        },

        {
          number: 2,
          name: 'Jack Nunge',
          height: "6'11",
          weight: 235,
          year: 'Soph',
          position: 'F',
          highschool: 'Castle',
          hometown: 'Newburgh, IN'
        },

        {
          number: 3,
          name: 'Jason Bohannon',
          height: "6'1",
          weight: 185,
          year: 'Jr',
          position: 'G',
          highschool: 'Linn-Mar',
          hometown: 'Marion, IA'
        },

        {
          number: 4,
          name: 'Isaiah Moss',
          height: "6'5",
          weight: 208,
          year: 'R-Jr',
          position: 'G',
          highschool: 'Simeon',
          hometown: 'Chicago, IL'
        },

        {
          number: 5,
          name: 'CJ Fredrick',
          height: "6'3",
          weight: 190,
          year: 'Fr',
          position: 'G',
          highschool: 'Covington',
          hometown: 'Cincinnati, OH'
        },

        {
          number: 10,
          name: 'Joe Wieskamp',
          height: "6'6",
          weight: 205,
          year: 'Fr',
          position: 'G',
          highschool: 'Muscatine',
          hometown: 'Muscatine, IA'
        },

        {
          number: 13,
          name: 'Austin Ash',
          height: "6'2",
          weight: 170,
          year: 'R-Fr',
          position: 'G',
          highschool: 'Mount Vernon',
          hometown: 'Cedar Rapids, IA'
        },

        {
          number: 15,
          name: 'Ryan Kriener',
          height: "6'9",
          weight: 255,
          year: 'Jr',
          position: 'F',
          highschool: 'Spirit Lake',
          hometown: 'Spirit Lake, IA'
        },

        {
          number: 20,
          name: 'Riley Till',
          height: "6'7",
          weight: 205,
          year: 'R-Jr',
          position: 'F',
          highschool: 'Wahlert',
          hometown: 'Dubuque, IA'
        },

        {
          number: 24,
          name: 'Nicolas Hobbs',
          height: "6'2",
          weight: 200,
          year: 'Soph',
          position: 'G',
          highschool: 'Fenwick',
          hometown: 'Chicago, IL'
        },

        {
          number: 25,
          name: 'Tyler Cook',
          height: "6'9",
          weight: 250,
          year: 'Jr',
          position: 'F',
          highschool: 'Chaminade Prep',
          hometown: 'St. Louis, MO'
        },

        {
          number: 30,
          name: 'Connor McCaffery',
          height: "6'5",
          weight: 205,
          year: 'R-Fr',
          position: 'G',
          highschool: 'West',
          hometown: 'Iowa City, IA'
        },

        {
          number: 35,
          name: 'Cordell Pemsl',
          height: "6'8",
          weight: 230,
          year: 'Jr',
          position: 'F',
          highschool: 'Wahlert',
          hometown: 'Dubuque, IA'
        },

        {
          number: 51,
          name: 'Nicholas Baer',
          height: "6'7",
          weight: 218,
          year: 'R-Sr',
          position: 'F',
          highschool: 'Bettendorf',
          hometown: 'Bettendorf, IA'
        },

        {
          number: 55,
          name: 'Luka Garza',
          height: "6'11",
          weight: 245,
          year: 'Soph',
          position: 'C',
          highschool: 'Maret School',
          hometown: 'Washington, D.C.'
        }
      ],

      coaches: [
        {
          name: 'Fran McCaffery',
          position: 'Head Coach'
        },
        {
          name: 'Kirk Speraw',
          position: 'Assistant Coach'
        },
        {
          name: 'Sherman Dillard',
          position: 'Assistant Coach'
        },
        {
          name: 'Andrew Francis',
          position: 'Assistant Coach'
        },
        {
          name: 'Courtney Eldridge',
          position: 'Video Coordinator'
        },
        {
          name: 'Al Seibert',
          position: 'Director of Operations'
        },
        {
          name: 'Brad Floy',
          position: 'Assistant Athletic Trainer'
        }
      ],

      games: [
        {
          date: 'Nov 4th',
          time: '2:05',
          opponent: 'Guliford College',
          location: 'Iowa City, IA',
          details: 'TV: BTN PLUS RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Nov 8th',
          time: '7:05',
          opponent: 'UMKC',
          location: 'Iowa City, IA',
          details: 'TV: BTN PLUS RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Nov 11th',
          time: '2:05',
          opponent: 'Green Bay',
          location: 'Iowa City, IA',
          details: 'TV: BTN PLUS RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Nov 15th',
          time: '8:15',
          opponent: 'Oregon',
          location: 'New York, NY',
          details: 'TV: ESPN2 RADIO: HAWKEYE SPORTS NETWORK'
        },
        {
          date: 'Nov 16th',
          time: '3:30/5:45',
          opponent: 'Syracuse/UConn',
          location: 'New York, NY',
          details: 'TV: ESPN2 RADIO: HAWKEYE SPORTS NETWORK'
        },
        {
          date: 'Nov 21st',
          time: '7:30',
          opponent: 'Alabama State',
          location: 'Iowa City, IA',
          details: 'TV: BTN PLUS RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Nov 27th',
          time: '8:00',
          opponent: 'Pittsburgh',
          location: 'Iowa City, IA',
          details: 'TV: ESPNU RADIO: HAWKEYE SPORTS NETWORK'
        },
        {
          date: 'Nov 30th',
          time: '7:00',
          opponent: 'Wisconsin',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Dec 3rd',
          time: '5:30',
          opponent: 'Michigan State',
          location: 'East Lansing, MI',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Dec 6th',
          time: '7:00',
          opponent: 'Iowa State',
          location: 'Iowa City, IA',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Dec.15th',
          time: '6:00',
          opponent: 'Northern Iowa',
          location: 'Des Moines, IA',
          details: 'TV: BTN RADIO: HAWKEYE SPORTS NETWORK'
        },
        {
          date: 'Dec 18th',
          time: '8:00',
          opponent: 'Western Carolina',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Dec 22nd',
          time: 'Noon',
          opponent: 'Savannah State',
          location: 'Iowa City, IA',
          details: 'TV: BTN PLUS RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Dec 29th',
          time: '7:00',
          opponent: 'Bryant',
          location: 'Iowa City, IA',
          details: 'TV: ESPNU RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 3rd',
          time: '6:00',
          opponent: 'Purdue',
          location: 'West Lafayette, IN',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 6th',
          time: '2:15/4:00',
          opponent: 'Nebraska',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 9th',
          time: '8:00',
          opponent: 'Northwestern',
          location: 'Evanston, ILL',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 12th',
          time: '1:30',
          opponent: 'Ohio State',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 16th',
          time: '6:00',
          opponent: 'Penn State',
          location: 'University Park, PA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 20th',
          time: 'Noon',
          opponent: 'Illinois',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 24th',
          time: '6:00',
          opponent: 'Michigan State',
          location: 'Iowa City, IA',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Jan 27th',
          time: '4:00',
          opponent: 'Minnesota',
          location: 'Minneapolis, MN',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 1st',
          time: '6:00',
          opponent: 'Michigan',
          location: 'Iowa City, IA',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 7th',
          time: '8:00',
          opponent: 'Indiana',
          location: 'Bloomington, IN',
          details: 'TV: ESPN/ESPN2 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 10th',
          time: '5:30',
          opponent: 'Northwestern',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 16th',
          time: '5:00',
          opponent: 'Rutgers',
          location: 'Piscataway, NJ',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 10th',
          time: '5:30',
          opponent: 'Northwestern',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 19th',
          time: '7:00',
          opponent: 'Maryland',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 22nd',
          time: '8:00',
          opponent: 'Indiana',
          location: 'Iowa City, IA',
          details: 'TV: FS1 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Feb 26th',
          time: '6:00',
          opponent: 'Ohio State',
          location: 'Columbus, OH',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'March 2nd',
          time: '4:00',
          opponent: 'Penn State',
          location: 'Iowa City, IA',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Mar 7th',
          time: '6:00',
          opponent: 'Wisconsin',
          location: 'Madison, WI',
          details: 'TV: ESPN/ESPN2 RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Mar 10th',
          time: '1:00',
          opponent: 'Nebraska',
          location: 'Lincoln, NE',
          details: 'TV: BTN RADIO: HAWKEYE RADIO NETWORK'
        },
        {
          date: 'Mar 13-17th',
          time: 'TBD',
          opponent: 'Big Ten Tournament',
          location: 'Chicago, IL',
          details: 'TBD'
        },
      ]
    };
  }
};
</script>

<style>
.fade-enter {
  opacity: 0;
}
.fade-enter-active {
  transition: opacity 1s;
}
.fade-leave {
  /* opacity: 1; */
  /* No reason to set opacity. It is 1 by default */
}
.fade-leave-active {
  transition: opacity 1s;
  opacity: 0;
}
body {
  height: 100vh;
  width: 100%;
  background-color: #000;
  background-image: url(./assets/hawkeye-wallpaper.jpg);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.links {
  margin-top: 5%;
}
.links h3 {
  color: gold;
  cursor: pointer;
  font-style: italic;
  text-decoration: underline;
  font-weight: 700;
}
</style>
