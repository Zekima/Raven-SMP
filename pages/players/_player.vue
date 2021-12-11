<template>
  <div>
    <rmenu></rmenu>
    <div class="under">
    <div class="players">
      <h2>{{stats.name}}</h2>
      <canvas id="skin_container" class="center"></canvas>
    </div>
    </div>
    <rfooter></rfooter>
  </div>
</template>
<style>

.players {
  padding-top: 20px;
}

.players h2{
  font-family: sofial;
  text-align: center;
  color: white;
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

