<template>
  <div id="app">
    <section>
      <div class="section__header">
        <h2>Matches</h2>
      </div>
      <div class="section__content">
        <Matches v-for="(item) in matchesList" v-bind:match="item" v-bind:key="item.id"/>
      </div>
    </section>
  </div>
</template>

<script>
import Matches from './components/Matches'

export default {
  name: 'app',
  components: {
    Matches
  },
  data () {
    return {
      matchesList: [
        {
          id: 1,
          team1: {
            name: 'Vitality',
            logo: 'https://static.hltv.org/images/team/logo/9565',
            score: 2,
          },
          team2: {
            name: 'ForZe',
            logo: 'https://static.hltv.org/images/team/logo/8135',
            score: 1,
          },
        },
        {
          id: 2,
          team1: {
            name: 'Na`Vi',
            logo: 'https://static.hltv.org/images/team/logo/4608',
            score: 2,
          },
          team2: {
            name: 'mousesports',
            logo: 'https://static.hltv.org/images/team/logo/4494',
            score: 1,
          },
        },
        {
          id: 3,
          team1: {
            name: 'Heroic',
            logo: 'https://static.hltv.org/images/team/logo/7175',
            score: 0
          },
          team2: {
            name: 'Virtus.pro',
            logo: 'https://static.hltv.org/images/team/logo/5378',
            score: 2
          },
        },
        {
          id: 4,
          team1: {
            name: 'Heroic',
            logo: 'https://static.hltv.org/images/team/logo/7175',
            score: '-',
          },
          team2: {
            name: 'Virtus.pro',
            logo: 'https://static.hltv.org/images/team/logo/5378',
            score: '-',
          },
        },
        {
          id: 5,
          team1: {
            name: 'Vitality',
            logo: 'https://static.hltv.org/images/team/logo/9565',
            score: '-',
          },
          team2: {
            name: 'ForZe',
            logo: 'https://static.hltv.org/images/team/logo/8135',
            score: '-',
          },
        },
        {
          id: 6,
          team1: {
            name: 'Na`Vi',
            logo: 'https://static.hltv.org/images/team/logo/4608',
            score: '-',
          },
          team2: {
            name: 'mousesports',
            logo: 'https://static.hltv.org/images/team/logo/4494',
            score: '-',
          },
        },
      ]
    }
  }
}
</script>

<style>
body {
  background-color: #1b1f23;
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0 auto;
  width: 1280px;
}

.section__header {
  display: flex;
  color: white;
}

.section__content {
  display: grid;
  flex-wrap: wrap;
  grid-gap: 12px;
  grid-template-columns: repeat(3, 1fr);
}
</style>
