<template>
<button @click="onClick">{{ name}}</button>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    name: String,
    onClick : Function,
  },
})
export default class Button extends Vue {
  name!: string
}
</script>

<style>
button {
  width: 250px;
  margin: 15px;
  color: Black;
  border-radius: 10px;
  background-color: burlywood;

}
</style>
