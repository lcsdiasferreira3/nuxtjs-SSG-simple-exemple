<template>
  <div>
    <v-row>
      <v-col cols="12" class="d-flex justify-center size1 pa-10">
        Produtos em Destaque - MacBook
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
              <img width="200px" :src="i.image" />
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
          name: 'MACBOOK AIR',
          priceFrom: 'R$ 25,000',
          priceTo: 'R$ 20,500',
          image:
            'https://s2.glbimg.com/olcxSKSBLBqiwJFQx_L7Cqo56rI=/0x0:695x381/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_08fbf48bc0524877943fe86e43087e7a/internal_photos/bs/2017/D/i/YCj97YTBSZLBqUfBA6Qw/macbook-air.png',
        },
        {
          name: 'MACBOOK PRO',
          priceFrom: 'R$ 18,000',
          priceTo: 'R$ 15,500',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/mbp-spacegray-select-202206?wid=904&hei=840&fmt=jpeg&qlt=90&.v=1653493200207',
        },
        {
          name: 'MACBOOK PRO 13 Polegadas',
          priceFrom: 'R$ 50,000',
          priceTo: 'R$ 34,500',
          image:
            'https://www.acronsoft.com.br/wp-content/uploads/2021/02/MacBookPro13M1_05.jpg',
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
