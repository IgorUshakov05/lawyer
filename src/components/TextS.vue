<template>
  <p style="user-select: none;" class="case">{{text}}</p>
</template>

<script>
export default {
  name: "TextSs",
  props: {
    text: {
type: String,
      required:true

    }
  }
}
</script>

<style scoped>

</style>