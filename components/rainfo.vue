<template>
  <div>
    <div class="info" id="1">
      <div class="linfo extra">
        <h1>What is a private server?</h1><br>
        <p>A private server allows you to experience Minecraft in the way it was intended. In a public server who knows if your house will still be there the next day.  </p>
      </div>
      <div class="rinfo">
        <img src="../static/assets/ogs.webp" class="center" alt="" style="margin-top:20px;">
      </div>
    </div>
    <hr>
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
    <hr>

    <div class="faq"><br>
      <h1>FAQ</h1>
      <div class="faq">
        <img src="../static/assets/faq.webp" alt="">
      </div>
  </div>
  </div>
</template>


<style>

.faq img {
  width: 150px !important;margin-top: 50px;}

.faq {text-align: center;}

.info {
  width: 1100px;
  font: lighter;
  height: 450px;
  font-family: sofial !important;
  text-align: left;
  display: flex;
  align-items: center;
  margin: 0 auto;
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

  }

.info p {
  font-size: 18px;
  }

  .v-expansion-panel--active:not(:first-child), .v-expansion-panel--active + .v-expansion-panel {
    margin-top: 1px !important;
}




.info img {
  display: block;
  width: 500px;

}

.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}

hr{background-color: #ccc;
        border: none; height: 1px;}





</style>


