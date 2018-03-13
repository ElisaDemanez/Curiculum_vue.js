<template>
  <div id="app">
<v-app light>

<navbar/>
  <v-content>
<toolbar/>
    <v-container fluid>
      <router-view/>

    </v-container>
  </v-content>


  <!-- <v-footer app>@2018</v-footer>  -->
  </v-app>
  </div>
</template>

<script>
import Navbar from './components/menu/navbar';
import Toolbar from './components/menu/toolbar';


export default {
  name: 'App', 
   data () {
      return {
        
      }
    },
    components: {
    'navbar': Navbar,
    'toolbar': Toolbar, 

  }
}
</script>

<style>
.height-auto {
height: auto;
}

#app {
  font-family: 'Roboto';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>


