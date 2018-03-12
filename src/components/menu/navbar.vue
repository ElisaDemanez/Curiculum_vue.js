
<template>
  <v-navigation-drawer permanent class="nav-bar blue lighten-3 pt-4" dark app>
    <v-toolbar flat class="transparent">
        <v-list class="pa-0">
          <v-list-tile avatar>
         
            <v-list-tile-content>
              <v-list-tile-title class="text-xs-center display-1 height-auto">Elisa Demanez</v-list-tile-title>
                    <v-list-tile-title class="text-xs-center display-0 height-auto">{{nav.age}}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-toolbar>


      <!-- list of items -->
    <v-list class=" pt-4">
      <v-list-tile v-for="item in navItems" :key="item.title" @click="">
        <v-list-tile-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
    <p>n°tel</p>
    <p>email: demanez.elisa@gmail.com</p>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
        navItems: [
          { title: 'Accueil', icon: 'dashboard' },
          { title: 'Compétences', icon: 'account_box' },
          { title: 'Expérience', icon: 'gavel' },
          { title: 'Formation', icon: 'gavel' },
          { title: 'Loisirs', icon: 'gavel' },
          { title: 'Contact', icon: 'gavel' }
                  
          
        ],
        nav:  {age: '20 ans?'}
  }
}
}
</script>