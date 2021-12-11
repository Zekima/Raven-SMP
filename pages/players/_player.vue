<template>
  <div>
    <rmenu></rmenu>
    <div class="under">
    <div class="players">
      <h2>{{stats.name}}</h2>
      <canvas id="skin_container" class="center"></canvas>
      <div class="statbg"><h4>Advancements:</h4><p>{{stats.points}}</p></div>
      <div class="statbg"><h4>Time Played:</h4><p>{{stats.time}} h</p></div>
      <div class="statbg"><h4>Deaths:</h4><p>{{stats.deaths}}</p></div>
      <div class="statbg"><h4>Kills:</h4><p>{{stats.kills}}</p></div>
    </div>
    </div>
    <rfooter></rfooter>
  </div>
</template>
<style>

.players {
  padding-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.players h2{
  font-family: mc;
  text-align: center;
  color: white;
  width: auto;
  padding-right: 5px;
  padding-left: 5px;
  padding-top: 2px;
  padding-bottom: 2px;
  font-weight: lighter;
  background-color: rgba(0, 0, 0, 0.178);

}

div.statbg {
  width: 208px;
  height: 40px;
  background-image: url(/assets/statbg.webp);
  font-family: mc;
  font-size: 20px;
  color: white;
  float: left;
  font-weight: lighter;
  display: flex;
  margin-top: 5px;
}

.statbg h4 {
  color: #fcfc00;
  margin-left: 9px;
  padding-top: 9px;

}

.statbg p {
  margin-left: 6px;
  padding-top: 9px;
}

</style>



<script>
import Rfooter from '../../components/rfooter.vue'
import rmenu from '../../components/rmenu.vue'
export default {
  components: { rmenu, Rfooter },
    data() {
      return {
        craft: "https://crafatar.com/skins/",
      }
    },

  async asyncData({route, redirect}) {
    const stats = await fetch(
      `https://ravenexpress.herokuapp.com/api/chirps/`+route.path.split('/').pop()
    ).then((res) => res.json())

    return { stats }
  },
  mounted() {
    setTimeout(() => {
    var skinview3d = require('skinview3d')
    var control, handles = {}
    var skinParts = {}
    let skinViewer = new skinview3d.SkinViewer({
		canvas: document.getElementById("skin_container"),
		width: 200,
		height: 400,

		skin: "https://crafatar.com/skins/" + this.stats.uuid
	});

    skinViewer.loadCape("https://crafatar.com/capes/" + this.stats.uuid)

                function walk() {
                    if (handles.run) {
                        handles.run.remove()
                        delete handles.run
                    }
                    handles.walk = handles.walk || skinViewer.animations.add(skinview3d.WalkingAnimation)
                }

                                function rotate() {
                    if (handles.rotate) {
                        handles.rotate.paused = !handles.rotate.paused
                    } else {
                        handles.rotate = skinViewer.animations.add(skinview3d.RotatingAnimation)
                    }
                }

                rotate()



  }, 0)
},



}
</script>

