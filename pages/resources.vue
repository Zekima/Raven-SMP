<template>
  <div>
    <rmenu></rmenu>
    <div class="resources">
      <div class="rahero">
        <h1>Everything used in Raven SMP</h1>
        <img src="../static/assets/work.webp" alt="" width="1200px" style="margin-top:40px">
      </div>
    </div>
    <div class="content">
      <div class="datapacks">
        <h3>Datapacks</h3>
        <div class="wrap">
        <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/vt.png" width="64px">
          </div>
          <div class="ctext">

            <h4>Vanilla Tweaks</h4>
            <p>Tweaks parts of the vanilla game</p>
          </div>
        </div>
                <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/blaze.png" width="64px">
          </div>
          <div class="ctext">

            <h4>Blaze and Caves</h4>
            <p>Adds 900+ advancements</p>
          </div>
        </div>
                <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/rand.png" width="64px">
          </div>
          <div class="ctext">

            <h4>Villager Names</h4>
            <p>Generates villager names</p>
          </div>
        </div>
                <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/zomb.png" width="64px">
          </div>
          <div class="ctext">

            <h4>Zombie Horsemen</h4>
            <p>Allows horsemen to spawn</p>
          </div>
        </div>
        </div>


      </div>
      <div class="plugins">
        <h3>Plugins</h3>
        <div class="wrap">
        <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/leaderboard.png" width="64px">
          </div>
          <div class="ctext">

            <h4>Leaderboard</h4>
            <p>Advancement leaderboard</p>
          </div>
        </div>
                <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/ri.png" width="64px">
          </div>
          <div class="ctext">

            <h4>Dynmap</h4>
            <p>Google maps for Minecraft</p>
          </div>
        </div>
                        <div class="ccard">
          <div class="cimg">
            <img src="../static/assets/ch.jpg" width="64px">
          </div>
          <div class="ctext">

            <h4>Chunky</h4>
            <p>Pre-generates chunks</p>
          </div>
        </div>
        </div>

      </div>
    </div>
  <rfooter></rfooter>
  </div>
</template>

<style>
.resources {
  width: 100%;
  height: 300px;
  color: white;
  background-color: #4d1d9e;
}


.rahero {
  margin: 0 auto;
  padding-top: 60px;
  max-width: 1100px;

}

.content {

  max-width: 1100px;
  height: 61vh;
  margin: 0 auto;
  font-family: sofial;
}

.content h3 {
  margin-top: 20px;
  margin-bottom: 20px;
  text-align: center;
  }

.wrap {
  justify-content: center;
  flex-wrap: wrap;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  max-width: 1100px;
}

.ccard {
  background-color: #edf2f7;
  border-radius: 10px;
  margin-right: 10px;
  margin-bottom: 10px;

  width: 245px;
  height: 75px;
 }

 .ctext{
   float: left;
   width: 55%;
   padding-top: 5px;

 }
.cimg{
   width: 35%;
   float: left;
   display: flex;
   justify-content: center;
   padding-top: 5px;
 }

 .datapacks {
   height: auto;
 }
 .plugins {
   height: auto;
 }


</style>
