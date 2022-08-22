<template>
  <div class="">
    <v-row>
      <v-col cols="6" class="d-flex justify-end">
        <p class="size">
          <strong>Loja.</strong>
          <span class="color"
            >O melhor jeito de <br /><span>comprar o que você ama.</span></span
          >
        </p>
      </v-col>
      <v-col cols="6"></v-col>
    </v-row>
    <v-row>
      <v-col cols="12" class="d-flex justify-center pb-10">
        <v-sheet class="mx-auto" elevation="8" max-width="80%" height="400px">
          <v-slide-group v-model="model" center-active show-arrows>
            <v-slide-item v-for="(i, index) in itens" :key="index">
              <v-card
                class="ma-4"
                height="370px"
                width="400px"
                dark
                :img="i.image"
                :to="'/' + i.to"
              >
                <div class="pa-5">
                  <span class="size1"> {{ i.name }}</span> <br />
                  <span class="size2">
                    {{ i.textSubtitle }}
                  </span>
                </div>
              </v-card>
            </v-slide-item>
          </v-slide-group>
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
      model: null,
      itens: [
        {
          name: 'IPHONE 13',
          textTitle: 'Seu novo superpoder',
          textSubtitle: 'Em todas as cores, mas agora em verde.',
          to: 'Iphone',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/store-card-40-iphone-13-pro-202203?wid=400&hei=500&fmt=p-jpg&qlt=95&.v=1645052290504',
        },
        {
          name: 'MACBOOK PRO DE 13 POL',
          textTitle: 'Pro em qualquer lugar.',
          textSubtitle: 'Tenha o poder da tecnologia em sua escrivaninha.',
          to: 'Mac',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/store-card-40-macbook-pro-202206?wid=400&hei=500&fmt=p-jpg&qlt=95&.v=1652803481192',
        },
        {
          name: 'IPAD AIR',
          textTitle: 'Cor e potência no ar.',
          textSubtitle: 'O poder na palma da mão.',
          to: 'IPad',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/store-card-40-ipad-air-202203?wid=400&hei=500&fmt=p-jpg&qlt=95&.v=1645636337374',
        },
        {
          name: 'ACESSÓRIOS',
          textTitle: 'Novas cores.',
          textSubtitle: 'Para seus acessórios favoritos çançarem tendência.',
          image:
            'https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/store-card-40-accesories-pride-202205?wid=400&hei=500&fmt=p-jpg&qlt=95&.v=1652291812834',
        },
      ],
    }
  },
}
</script>

<style scoped>
.size {
  font-size: 50px;
}
.size1 {
  font-size: 30px;
  font-weight: 700;
  color: rgb(179, 170, 170);
}
.size2 {
  font-size: 13px;
  font-weight: 500;
  color: rgb(177, 177, 233);
}
.color {
  color: rgb(160, 160, 160);
}
</style>
