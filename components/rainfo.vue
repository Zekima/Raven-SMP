<template>
  <div>
    <div class="info" id="1">
      <div class="linfo extra">
        <h1>What is a private server?</h1><br>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean finibus lectus leo, sed tincidunt dolor iaculis nec. Suspendisse non rutrum mauris, ac lacinia tortor. Sed rhoncus diam et magna viverra gravida. Suspendisse vulputate vel neque id bibendum. Cras in felis facilisis, mattis neque vitae, congue massa. Phasellus ultrices elit ac metus luctus ultrices.</p>
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
        <h1>You will not get banned for nothing</h1><br>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean finibus lectus leo, sed tincidunt dolor iaculis nec. Suspendisse non rutrum mauris, ac lacinia tortor. Sed rhoncus diam et magna viverra gravida. Suspendisse vulputate vel neque id bibendum. Cras in felis facilisis, mattis neque vitae, congue massa. Phasellus ultrices elit ac metus luctus ultrices.</p>
      </div>
    </div>
    <hr>

    <div class="info">
      <h1>FAQ</h1>
      <div class="faq">

        <img src="../static/assets/faq.webp" alt="">

      </div>





              <v-row justify="center" >
    <v-expansion-panels accordion class="accord">
      <div style="width:80%;justify-content: flex-end;">
      <v-expansion-panel>
        <v-expansion-panel-header>Do you need a license to play on the server?</v-expansion-panel-header>
        <v-expansion-panel-content>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </v-expansion-panel-content>
      </v-expansion-panel>
            <v-expansion-panel>
        <v-expansion-panel-header>What will happen to my things and buildings if I get ripped off?</v-expansion-panel-header>
        <v-expansion-panel-content>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </v-expansion-panel-content>
      </v-expansion-panel>
            <v-expansion-panel>
        <v-expansion-panel-header>Item</v-expansion-panel-header>
        <v-expansion-panel-content>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </v-expansion-panel-content>
      </v-expansion-panel>
            <v-expansion-panel>
        <v-expansion-panel-header>Item</v-expansion-panel-header>
        <v-expansion-panel-content>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </v-expansion-panel-content>
      </v-expansion-panel>
      </div>
    </v-expansion-panels>


  </v-row>
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


