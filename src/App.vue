<template>
<OneComponent />
  <div class="app">
<IamProfile />
    <Team />
    <Team2 />
    <Usluga />
    <Contact />
  </div>
<foot />
</template>

<script>
import OneComponent from './components/HelloWorld.vue'
import IamProfile from './components/Iam.vue'
import Team from './components/Team.vue'
import Team2 from './components/TeamTwos.vue'
import Foot from './components/foot.vue'
import Usluga from './components/usluga.vue'
import Contact from './components/contact.vue'

export default {
  name: 'App',
  components: {
    OneComponent,
    IamProfile,
    Team,
    Team2,
    Foot,
    Usluga,
    Contact
  }
}
</script>

<style>
.app {
  max-width: 1300px;
  margin: auto;
  position: relative;
}

</style>
