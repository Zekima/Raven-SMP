<template>
  <div>
    <div class="info" id="1">
      <div class="linfo extra">
        <h1>What is a private server?</h1><br>
        <p>A private server allows you to experience Minecraft in the way it was intended. In a public server who knows if your house will still be there the next day.
          <br><br>Raven SMP is a community consisting of people from all over the world comming together to play the game that we love, Minecraft.
        </p>
      </div>
      <div class="rinfo">
        <img src="../static/assets/ogs.webp" class="center" alt="" style="margin-top:20px;">
      </div>
    </div>
    <div class="info">
      <div class="rinfo">
        <img src="../static/assets/rulesfi.webp" class="center" alt="">
      </div>
        <div class="linfo extra">
        <h1>Server Rules & Restrictions</h1><br>
        <p>To keep the community safe and civil there are couple rules to follow </p>
        <br>
        <ul class="list">
          <li>Do not be disrespectful!</li>
          <li>Definitely do not be racist, homophobic, sexist etc!</li>
          <li>Do not grief.</li>
          <li>Do not do harmful pranks, e.g fill their house with lava.</li>
          <li>No hacking!</li>
        </ul>
      </div>
    </div>
        <div class="info">

    </div>
    <div class="join">
      <h1>Ready to join our community?</h1>
      <a href="apply"><button class="app">Applications</button></a>
    </div>



    </div>
</template>


<style>


.faq {text-align: center;width: 90px !important; float: left;}

.info {
  max-width: 1100px;
  font: lighter;
  max-height: 450px;
  text-align: left;
  margin: 0 auto;
  margin-bottom: 50px;
}

.extra {

}

.accord { justify-content: end;}


.hidden {
  display: none;
}
.list {
  list-style-type: decimal;
  margin-left: 20px;
}
.linfo, .rinfo {
  width: 50%;
  float: left;
  margin-bottom: 100px;


  }

.info p {
  font-size: 18px;
  color: #1a1a1a;
  font-family: sofial;
  }

  .v-expansion-panel--active:not(:first-child), .v-expansion-panel--active + .v-expansion-panel {
    margin-top: 1px !important;
}




.info img {
  display: block;
  width: 500px;

}

.join {
  width: 100%;
  background-color: black;
  color: white;
  float: left;
  text-align: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  font-family: sofial;
  height: 200px;
}

.join button {

    padding: 9px;
    font-size: 18px;
    border-radius: 9px;
    margin-top: 10px;
    border: 0;
    width: 175px;
    cursor: pointer;
    background-color: white !important;
    color: black;
    font-family: sofiam;
}

.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}

hr{background-color: #ccc;
        border: none; height: 1px;}

  .extra {
    padding: 50px;
    padding-top: 100px;
    box-sizing: border-box;
  }



</style>


