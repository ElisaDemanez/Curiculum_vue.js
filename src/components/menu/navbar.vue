
<template>
  <v-navigation-drawer permanent class="nav-bar grey darken-1 pt-4" dark app>
    <v-toolbar flat class="transparent">
        <v-list class="pa-0">
          <v-list-tile avatar>
         
            <v-list-tile-content>
              <v-list-tile-title class="text-xs-center display-1 height-auto">Elisa Demanez</v-list-tile-title>
                    <v-list-tile-title class="text-xs-center display-0 height-auto">{{age[$root.currentLocale]}}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-toolbar>


      <!-- list of items -->
    <v-list class=" pt-4">
      <v-list-tile v-for="item in navItems[$root.currentLocale]" :key="item.title" @click="">
        <v-list-tile-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
        <v-card-text>
 
      <p class="text-xs-center white--text"><v-icon>dashboard</v-icon>n° 00 00000</p>
      <p class="text-xs-center white--text"><v-icon>dashboard</v-icon>demanez.elisa@gmail.com</p>
      
    </v-card-text>

    <v-layout wrap justify-space-around align-center>
        <v-avatar class="indigo">
        <v-icon dark>account_circle</v-icon>
        </v-avatar>
        <!-- <v-avatar>
        <img src="/static/doc-images/john.jpg" alt="John">
        </v-avatar> -->
        <v-badge overlap>
        <span slot="badge">3</span>
        <v-avatar
            class="purple red--after"
        >
            <v-icon dark>notifications</v-icon>
        </v-avatar>
        </v-badge>
       
        <v-avatar class="red">
        <span class="white--text headline">J</span>
        </v-avatar>
    </v-layout>


    </v-navigation-drawer>
</template>

<script>

import root from '../../main.js'
export default {
  name: 'Navbar',
  data () {
    return {
        
        navItems: { fr : [
          { title: 'Accueil', icon: 'home' },
          { title: 'Compétences', icon: 'account_box' },
          { title: 'Expérience', icon: 'gavel' },
          { title: 'Formation', icon: 'gavel' },
          { title: 'Loisirs', icon: 'gavel' },
          { title: 'Contact', icon: 'gavel' }
                  
          
        ],
        en : [
          { title: 'Home', icon: 'home' },
          { title: 'Skills', icon: 'account_box' },
          { title: 'Work experience', icon: 'gavel' },
          { title: 'Education', icon: 'gavel' },
          { title: 'Hobbies', icon: 'gavel' },
          { title: 'Contact', icon: 'gavel' }
                  
        ]
        },
        age:  {fr : '20 ans', en : '20 years old'},
        
        
  }
  
}
}
</script>