<template>
  <div>
    <rmenu></rmenu>

    <div class="under">
          <div class="top">
          <div class="prel">
            <h1>Leaderboard</h1>
            <p>Points = Advancements</p>
          </div><br>
      <div class="lcard" :class="{ 'active': index === 0,  'active2': index === 1, 'active3': index === 2 }"  v-for="(stat,index) in sortedArray" :key="stat.name" >
        <p class="nrr">{{ index+1 }}.</p><img :src="craft + stat.uuid + '?scale=2&overlay'" /><nuxt-link :to="`/players/${stat.name}`"><p class="pname">{{ stat.name }}</p></nuxt-link>
        <div class="ppos">
                  <p class="points">{{ stat.points }} Points</p>
        </div>
      </div>
    </div>
    </div>

    <div class="bottom"></div>
    <rfooter></rfooter>

  </div>
</template>



<style>

.prel{
  width: 100%;
  color: white;
  text-align: center;
}

.prel p {
  font-family: sofial;
}
.under {
  width: 100%;
  min-height: 95vh;
  padding-bottom: 50px;
  background-color: #4d1d9e;
}
.active {
  flex: 0 1 30%;
}
.active2 {
 flex: 0 1 30%;
}
.active3 {
  flex: 0 1 30%;
}

.active .nrr {
  color: yellow;
}

.active2 .nrr {
  color: rgb(172, 172, 172);
}

.active3 .nrr {
  color: rgb(165, 122, 42);
}

.nrr{
  position: absolute;
  top: 5px;
  left: 15px;
}
.pname{text-align: center;}
.ppos {float: right; }
.top {
  max-width: 1100px;
  height: auto;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
}
.points {
  padding: 3px;
  background-color: #ffffff;
  color: black;
  border-radius: 10px;
  vertical-align: middle;
  margin-bottom: -10px;
}
.under h1{
  color: white;
  text-align: center;
  padding-top: 20px;
}
.under h5{
  color: white;
  text-align: center;
  padding-bottom: 20px;
  font-family: sofial !important;
}
.under a {
    color: rgb(255, 255, 255);
}
.under a:active {
    color: blue;
}
.under a[tabindex]:focus {
    color:blue;
    outline: none;
}
.lcard {
  background-color: #2a0f57;
  color: white;
  position: relative;

  margin-top: 20px;
  margin-right: 20px;
  border-radius: 10px;
  height: 150px;
  display: flex;
  float: left;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 150px;
  padding: 5px;
}
.lcard p {display: inline-block;}
</style>


<script>
  export default {
    data() {
      return {
        stats: [],
        craft: "https://crafatar.com/renders/body/",
      }
    },
    async fetch() {
      this.stats = await fetch(
        'https://ravenexpress.herokuapp.com/api/chirps'
      ).then(res => res.json())
    },
    computed: {
  sortedArray: function() {
    function compare(a, b) {
      if (a.points < b.points)
        return 1;
      if (a.points > b.points)
        return -1;
      return 0;
    }
    return this.stats.sort(compare);
  },
},
  template: `
    <div>
        v-for="(stat, index) in sortedArray"
        :class="{ 'active': index === 1 }"
        :text="stat.name 45">
    </div>
  `,
  }
</script>
