<template>
  <div>
    <v-row>
      <v-col cols="12" class="d-flex justify-center size1 pa-10">
        Produtos em Destaque - IPad
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
              <img width="170px" :src="i.image" />
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
          name: 'IPAD PRO 64g',
          priceFrom: 'R$ 4,000',
          priceTo: 'R$ 2,500',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-pro-12-select-wifi-silver-202104_GEO_BR_FMT_WHH?wid=940&hei=1112&fmt=p-jpg&qlt=95&.v=1617922555000',
        },
        {
          name: 'IPAD AIR 128g',
          priceFrom: 'R$ 3,000',
          priceTo: 'R$ 1,500',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-air-select-wifi-starlight-202203?wid=1765&hei=2000&fmt=jpeg&qlt=95&.v=1645895139236',
        },
        {
          name: 'IPAD MINI 32g',
          priceFrom: 'R$ 5,000',
          priceTo: 'R$ 2,500',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-mini-select-cell-pink-202109_FMT_WHH?wid=940&hei=1112&fmt=png-alpha&.v=1629840657000',
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
