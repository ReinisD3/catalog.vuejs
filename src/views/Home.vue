<template>
  <div class="home">
    <Button v-for="animal in animal_types " :name="animal"></Button>
    <br>
    <Image v-for="link in animal_images"   :src="link[0]" :class="link[1]" ></Image>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

import Button from '@/components/Button/Button.vue'; // @ is an alias to /src
import Image from '@/components/Image/Image.vue'; // @ is an alias to /src

@Options({
  components: {
    Button,
    Image,
  },
  data: () => ({
    animal_types: ['Cats','Dogs'],
    animal_images: [['https://d2zp5xs5cp8zlg.cloudfront.net/image-33998-800.jpg','dog'],
      ['https://img2.thejournal.ie/article/5170458/river?version=5170546&width=1340','dog'],
    ['https://i.natgeofe.com/n/3861de2a-04e6-45fd-aec8-02e7809f9d4e/02-cat-training-NationalGeographic_1484324_square.jpg', 'cat'],
    ['https://media.wired.com/photos/5cdefb92b86e041493d389df/2:1/w_1500,h_750,c_limit/Culture-Grumpy-Cat-487386121.jpg', 'cat'],
      ['https://cdn.vox-cdn.com/thumbor/39qOT2mBvSzyuLRthZyxxxSXDkg=/1400x1050/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/2449662/shutterstock_149489132.0.jpg', 'cat'],
      ['https://ggsc.s3.amazonaws.com/images/uploads/The_Science-Backed_Benefits_of_Being_a_Dog_Owner.jpg', 'dog']]
  })
})
export default class Home extends Vue {}
</script>
<style>
.dog{
  border: brown solid 5px;
}
.cat {
  border: darkgreen solid 5px;
}
</style>
