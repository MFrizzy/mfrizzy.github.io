<template>
  <v-container class="pb-0">
    <div class="display-1 pa-3">Timeline</div>
    <v-timeline :dense="$vuetify.breakpoint.xsOnly" class="timeline">
      <v-timeline-item v-for="item in items" :key="item.title" small fill-dot>
        <span slot="opposite">{{ item.date }}</span>
        <v-card class="elevation-2 card">
          <v-card-title class="headline">
            <span v-html="item.title"></span>
            <span v-if="$vuetify.breakpoint.xsOnly" class="subtitle-1 grey--text">{{ item.date }}</span>
          </v-card-title>
          <v-card-text v-html="item.text"></v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        date: "Mars 2019 - Maintenant",
        title:
          "Développeur front-end à <a target='_blank' href='https://jymiz.com'>Jymiz</a>",
        text:
          "Développement d'interfaces pour tous les systèmes liés à l'activité <a target='_blank' href='https://jymiz.com'>Jymiz</a>"
      },
      {
        date: "Avril 2018 - Juillet 2018",
        title: "Stage : développeur web",
        text:
          "Développement d'une solution de cartographie web via Leaflet pour l'<a target='_blank' href='https://oreme.org/'>OREME</a>"
      },
      {
        date: "Novembre 2017 - Maintenant",
        title: "Assesseur de publicité Google",
        text:
          "Assesseur à <a target='_blank' href='https://www.lionbridge.com/'>Lionbridge</a>"
      },
      {
        date: "2016 - 2018",
        title: "DUT : Informatique & Gestion",
        text: "A l'IUT de Montpellier, en option Anglais"
      }
    ]
  })
};
</script>
<style scoped>
.card {
  border-radius: 24px;
}

.timeline {
  max-width: 800px;
  margin: auto;
}
</style>

