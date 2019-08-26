<template>
  <v-container>
    <div class="home-layout" style="flex-wrap:1;">
      <div class="me-description pl-10">
        <div class="display-1">Tanguy</div>
        <div class="display-2">Thomas</div>
        <div class="headline">Full-stack développeur</div>
        <div>
          <v-btn text icon href="mailto:mfrizzy@pm.me" target="_blank">
            <v-icon>fa-at</v-icon>
          </v-btn>
          <v-btn text icon href="https://www.linkedin.com/in/tanguy-thomas" target="_blank">
            <v-icon>fab fa-linkedin-in</v-icon>
          </v-btn>
          <v-btn text icon href="http://www.github.com/mfrizzy" target="_blank">
            <v-icon>fab fa-github</v-icon>
          </v-btn>
          <v-btn text icon href="https://codepen.io/Mfrizzy/" target="_blank">
            <v-icon>fab fa-codepen</v-icon>
          </v-btn>
          <v-btn text icon href="https://kit.com/Mfrizzy" target="_blank">
            <img class="kit" src="kit.svg" />
          </v-btn>
        </div>
      </div>
      <v-spacer></v-spacer>
      <div class="cards">
        <v-card class="card ma-3">
          <v-img :src="publicPath + 'icons/desktop.svg'" class="card-img"></v-img>
          <v-card-title style="justify-content:center;">Front-end</v-card-title>
          <v-card-text class="text-center">
            HTML/CSS
            <br />JS (Vue)
            <br />Adobe XD / Figma
          </v-card-text>
        </v-card>
        <v-card class="card ma-3">
          <v-img :src="publicPath + 'icons/server.svg'" class="card-img"></v-img>
          <v-card-title style="justify-content:center;">Back-end</v-card-title>
          <v-card-text class="text-center">
            Php (Laravel)
            <br />NodeJS
            <br />SQL/PLSQL
          </v-card-text>
        </v-card>
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      publicPath: process.env.BASE_URL
    };
  }
};
</script>

<style scoped>
.me-description {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-width: 300px;
}

.home-layout {
  display: flex;
  flex-wrap: wrap;
  margin-top: 100px;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  margin: auto;
  justify-content: center;
}

@media (max-width: 873px) {
  .cards {
    padding-top: 100px;
  }
}

.card {
  min-width: 250px;
  border-radius: 24px;
}

.card-img {
  margin: 24px auto;
  width: 50%;
}

.kit {
  width: 24px;
  height: 24px;
}
</style>
