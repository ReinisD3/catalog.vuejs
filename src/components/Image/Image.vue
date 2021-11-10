<template>
  <img :src=source alt="Picture Here">
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    source: String
  }
})
export default class Image extends Vue {
  source!: string
}
</script>

<style>
img {
  width: 280px;
  height: 180px;
}
</style>
<!-- Add "scoped" attribute to limit CSS to this component only -->

