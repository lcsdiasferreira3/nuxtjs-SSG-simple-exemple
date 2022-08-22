<template>
  <div>
    <v-row>
      <v-col cols="12" class="d-flex justify-center size1 pa-10">
        Produtos em Destaque - IPhone
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" class="d-flex justify-center pb-10">
        <v-sheet
          class="mx-auto"
          elevation="8"
          max-width="80%"
          height="400px"
          color="grey"
          v-for="(i, index) in itens"
          :key="index"
        >
          <v-card class="ma-4" height="370px" width="400px" dark>
            <v-col cols="12" class="d-flex justify-center size">{{
              i.name
            }}</v-col>
            <v-col cols="12" class="d-flex justify-center align-center">
              <img width="250px" :src="i.image" />
              <v-rating
                color="red"
                empty-icon="mdi-heart-outline"
                full-icon="mdi-heart"
                length="1"
                value="0"
                size="30"
                class="position"
              ></v-rating>
            </v-col>
            <p class="d-flex justify-center mb-0">De: {{ i.priceFrom }}</p>
            <p class="d-flex justify-center">Por: {{ i.priceTo }}</p>
          </v-card>
        </v-sheet>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  data() {
    return {
      itens: [
        {
          name: 'IPHONE 10 64g',
          priceFrom: 'R$ 15,000',
          priceTo: 'R$ 12,500',
          image:
            'https://www.ephotozine.com/articles/apple-iphone-x-smartphone-camera-review--31851/images/highres-iPhoneX_1515578337.jpg',
        },
        {
          name: 'IPHONE 12 128g',
          priceFrom: 'R$ 12,000',
          priceTo: 'R$ 9,500',
          image: 'https://i.zst.com.br/thumbs/12/3e/39/-522515954.jpg',
        },
        {
          name: 'IPHONE 8 32g',
          priceFrom: 'R$ 20,000',
          priceTo: 'R$ 10,500',
          image:
            'https://a-static.mlcdn.com.br/574x431/iphone-8-apple-64gb-dourado-47-12mp-ios/magazineluiza/155542800/f111ab6ad814e5f4576b9080c483af08.jpg',
        },
      ],
      value: '',
    }
  },
}
</script>

<style scoped>
.size {
  font-size: 30px;
  font-weight: 700;
}
.size1 {
  font-size: 60px;
  font-weight: 700;
  color: rgb(255, 255, 255);
}
.position {
  position: absolute;
  left: 85%;
  bottom: 80%;
}
</style>
