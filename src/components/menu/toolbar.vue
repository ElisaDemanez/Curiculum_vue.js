
<template>
 <!-- scroll-threshold="100" -->
  <v-card color="grey lighten-4" flat height="200px" tile>
    <v-toolbar dense>
  
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>search</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>favorite</v-icon>
      </v-btn>
    
      <select v-model="currentLocale">
    <option v-for="locale in locales" v-bind:value="locale.id" v-on:click="lang(locale.id )">{{locale.name}}</option>
  </select>
   
    </v-toolbar>
  </v-card>
</template>

<script>


export default {
  name: 'Toolbar',
  data () {
    return {
      currentLocale:'fr',
    locales: [ {id: 'en', name: 'English'}, {id: 'fr', name: 'Français'}]

    }
  },
  //pass globally the lang var
  methods: {
  lang: function (selected) {
  
    this.$root.currentLocale = selected
  }
}
}
</script>