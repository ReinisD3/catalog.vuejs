<template>
  <div class="card" >
    <div >
      <h3 class="name">{{ animal.name }}</h3>
      <Image :src="animal.picture" :class="animal.type" ></Image>
    </div>

  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Image from '../Image/Image.vue';


@Options({
  components: {
    Image,
  },
  props: {
    animal: {
      type: Object
    },
    onClick : Function,
  },
})
export default class Animalcard extends Vue {
  name!: string
}
</script>

<style>
.card{
  background-color: grey;
  width: 320px;
  border: #2c3e50 solid 5px;
}
.dog{
  border: brown solid 3px;
}
.cat {
  border: darkgreen solid 3px;
}
.name{
  color:darkblue;
}
</style>
