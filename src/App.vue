<template>
  <div class="app-base">
    <img class="img-background" src="./assets/images/blablabackground.jpg" />
    <div class="overlay">
      <Headlines /> // <Minute /> // <MatchTabs /> // <TabContent />
    </div>
  </div>
</template>

<script>
import Headlines from "./components/Headlines";
export default {
  name: "App",
  components: {
    Headlines,
  },
};
</script>

<style>
* {
  margin: 0;
}
.app-base {
  width: 100vw;
  height: 100vh;
  background: black;
}

.img-background {
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  filter: blur(2px);
}

.overlay {
  width: 100%;
  height: 100%;
  position: absolute;
  background: #1d1d1da3;
  top: 0;
}
</style>
