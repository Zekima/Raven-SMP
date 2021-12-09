<template>
    <div class="menu">
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/leaderboard">Leaderboard</nuxt-link>
      <nuxt-link to="/map">Map</nuxt-link>
      <nuxt-link to="/resources">Resources</nuxt-link>
    </div>
</template>


<style>
a.nuxt-link-exact-active {
  color: #00c58e;

}


a.nuxt-link-exact-active:before {
  position: absolute;
  height: 2px;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #00c58e;
  border-radius: 2px 2px 0 0;
  }



</style>
