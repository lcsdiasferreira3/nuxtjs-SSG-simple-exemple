<template>
  <div>
    <v-app-bar height="55px" dark class="">
      <v-col cols="3"></v-col>
      <v-col cols="6">
        <v-row align="center" justify="space-around" class="d-flex">
          <NuxtLink to="/"
            ><img width="20px" class="mt-2" src="../assets/logo_apple.png"
          /></NuxtLink>
          <span v-for="(i, index) in itens" :key="index"
            ><NuxtLink :to="'/' + i.name">{{ i.name }}</NuxtLink></span
          >
          <v-icon></v-icon>
          <v-btn icon><v-icon>mdi-magnify</v-icon></v-btn>
          <v-btn icon> <v-icon>mdi-bag-checked</v-icon></v-btn>
        </v-row>
      </v-col>
      <v-col cols="3"></v-col>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itens: [
        {
          name: 'Mac',
        },
        {
          name: 'IPad',
        },
        {
          name: 'Iphone',
        },
        {
          name: 'Watch',
        },
        {
          name: 'AirPods',
        },
        {
          name: 'TV e Casa',
        },
        {
          name: 'Só na Apple',
        },
        {
          name: 'Acessórios',
        },
        {
          name: 'Suporte',
        },
      ],
    }
  },
}
</script>

<style>
a {
  text-decoration: none;
  color: white !important;
}
</style>
