<template>
<div class="team">
  <div class="teama">

  <hr>
  <div class="teams">
    <h2>Кто мы</h2>
  </div>
  </div>
</div>
</template>

<script>
import '../../public/fonts/SegoeUI.ttf'
export default {
  name: "TeamKaa",
}
</script>

<style scoped>
.team {
  width: 96%;
  margin: auto;
  margin-top: 100px;
}
p {
  font-family: "Segoe UI";
}
h2 {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 31.509px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%;
  letter-spacing: 2.206px;
}
hr {
  padding: 1px solid #242E87 ;
  background: #242E87;
}
.teama {
  position: relative;
}
.teams {
  width: fit-content;
  background: white;
  padding: 0 12px;
  margin: auto;

  position: absolute;
  text-align: center;
  right: 0;
  top: -29px;
  left: 0;
}
.teams > h2 {
  color: #313C98;
}
</style>