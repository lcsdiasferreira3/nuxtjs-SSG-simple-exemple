<template>
  <v-footer dark padless>
    <v-card flat tile width="100%">
      <v-card-text class="text-center">
        <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <div class="white--text pt-0 d-flex justify-space-around">
        <v-col cols="2">
          <p>
            <strong><h2>Descobrir e Comprar</h2></strong>
          </p>
          <p>Loja</p>
          <p>Mac</p>
          <p>IPad</p>
          <p>IPhone</p>
          <p>Watch</p>
        </v-col>
        <v-col cols="2"
          ><p>
            <strong><h2>Serviços</h2></strong>
          </p>
          <p>Apple Music</p>
          <p>Apple TV+</p>
          <p>Apple Fitness+</p>
          <p>Apple Arcade</p>
          <p>ICloud</p>
        </v-col>
        <v-col cols="2"
          ><p>
            <strong><h2>Apple Store</h2></strong>
          </p>
          <p>Encontre uma loja</p>
          <p>Genius Bar</p>
          <p>Today at Apple</p>
          <p>Apple Camp</p>
          <p>Apple Camp</p>
        </v-col>
        <v-col cols="2"
          ><p>
            <strong><h2>Para Empresas</h2></strong>
          </p>

          <p>Apple e os negócios</p>
          <p>Comprar para sua empresa</p>
          <p>Apple e a Educação</p>
          <p>Comprar para Educação Básica</p>
          <p>Comprar para a Faculdade</p>
        </v-col>
        <v-col cols="2"
          ><p>
            <strong><h2>Valores da Apple</h2></strong>
          </p>

          <p>Acessibilidade</p>
          <p>Meio Ambiente</p>
          <p>Privacidade</p>
          <p>Responsabilidade</p>
          <p>Newsroom</p></v-col
        >
      </div>

      <v-divider></v-divider>
      <div class="d-flex justify-space-around pa-10">
        <v-col cols="6" class="d-flex align-center justify-center">
          <span>
            © 2022 Apple Inc. Todos os direitos reservados. Apple Computer
            Brasil Ltda. CNPJ: 00.623.904/0003-35</span
          >
        </v-col>
        <v-col cols="6">
          <span class="white--text d-flex align-center justify-center">
            <span class="pr-4"
              ><h2>{{ new Date().getFullYear() }}</h2></span
            >
            <img width="30px" src="../assets/logo_apple.png" />
          </span>
        </v-col>
      </div>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {
      icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram'],
    }
  },
}
</script>

<style></style>
