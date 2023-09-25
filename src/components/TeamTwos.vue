<template>
  <div class="all">

  <PersonComnent3 />
  <Person />
  <PerComponent2 />
  </div>
  <div id="make"></div>
</template>

<script>
import PersonComnent3 from "@/components/Person3.vue";
import PerComponent2 from "@/components/Person2.vue";
import Person from "@/components/Person.vue";

export default {
  name: "teamTwo",
  components: {PersonComnent3,PerComponent2, Person}
}
</script>

<style scoped>
.all {
  margin-top: 50px;
}
</style>