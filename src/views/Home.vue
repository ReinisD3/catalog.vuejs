<template>
<Button v-for="type in buttonTypes" :name="type.type" @click="Show(type.type)"></Button>
<div class="grid">
  <div v-for="animal in animals"  >
    <Animalcard  :hidden="!animal.show"  :animal="animal"></Animalcard>
  </div>
</div>

</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Animalcard from '@/components/AnimalCard/Animalcard.vue';
import Button from '@/components/Button/Button.vue';

@Options({
  components: {
    Animalcard,
    Button,
  },
  data: () => ({
    buttonTypes: [{
      type: 'cat'
    },
      {
        type: 'dog'
      },
      {
        type: 'all'
      },],
    animals: [{
      type: 'dog',
      name: 'Pipars',
      picture: 'https://d2zp5xs5cp8zlg.cloudfront.net/image-33998-800.jpg',
      show: true
    },{
      type: 'dog',
      name: 'Adžika',
      picture: 'https://img2.thejournal.ie/article/5170458/river?version=5170546&width=1340',
      show: true
    },{
      type: 'cat',
      name: 'Grumpy',
      picture: 'https://media.wired.com/photos/5cdefb92b86e041493d389df/2:1/w_1500,h_750,c_limit/Culture-Grumpy-Cat-487386121.jpg',
      show: true
    },{
      type: 'cat',
      name: 'Platais Muris',
      picture: 'https://i.natgeofe.com/n/3861de2a-04e6-45fd-aec8-02e7809f9d4e/02-cat-training-NationalGeographic_1484324_square.jpg',
      show: true
    },{
      type: 'cat',
      name: 'Puffy',
      picture: 'https://cdn.vox-cdn.com/thumbor/39qOT2mBvSzyuLRthZyxxxSXDkg=/1400x1050/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/2449662/shutterstock_149489132.0.jpg',
      show: true
    },{
      type: 'dog',
      name: 'Niknais',
      picture: 'https://ggsc.s3.amazonaws.com/images/uploads/The_Science-Backed_Benefits_of_Being_a_Dog_Owner.jpg',
      show: true
    },
    ],
  }),
  methods: {
    Show(type: string){
      this.animals.forEach(function(animal: any) {
          animal.type == type ? animal.show = true : animal.show = false;
         if(type == 'all') animal.show = true;
            })

    }

  }

})
export default class Home extends Vue {}
</script>
<style>
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 15px;
  margin-left: 30px;

}
</style>
