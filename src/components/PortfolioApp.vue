<template>
  <v-card max-width="350px" class="mx-auto mb-5" :href="app.link" target="_blank">
    <v-img class="white--text align-end" height="200px" :src="logo(app.logo)">
      <v-card-title align="center" class="text-center text-shadow">{{app.name}}</v-card-title>
    </v-img>
    <v-card-subtitle class="pb-0">
      <v-layout>
        <v-flex xs5>
          <div class="caption"><v-icon size="18">mdi-account</v-icon> {{app.author}}</div>
        </v-flex>

        <v-flex xs4> 
          <div class="caption"><v-icon size="18">mdi-calendar</v-icon> {{app.date_created}}</div>
        </v-flex>

        <v-flex xs3>
          <div class="caption"><v-icon size="18">mdi-xml</v-icon> {{app.type}}</div>
        </v-flex>
      </v-layout>
    </v-card-subtitle>

    <v-card-text class="text--primary mt-3">
      <div>{{app.description}}</div>
    </v-card-text> 

    <v-card-text class="text--primary" align="center" justify="center">
      <div class="title">Tecnologias Aplicadas</div>
    </v-card-text> 

    <v-card-actions>
      <template v-for="(tech, i) in app.technologies">
        <v-flex xs3 :key="i">
          <div class="text-center" align="center" justify="center">
            <v-btn icon>
              <v-icon>{{tech.icon}}</v-icon>
            </v-btn>
            <div class="caption">{{tech.name}}</div>
          </div>
        </v-flex>
      </template>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    app: {
      type: Object,
      default: function() {
        return {};
      }
    }
  },
  methods: {
    logo(name) {
      return require("../assets/img/" + name);
    }
  }
};
</script>

<style>
.text-shadow {
	text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.3);
}
</style>