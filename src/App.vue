<template>

  <div class="main-container" :class="(dark_theme ? 'dark-theme':'')">
    <SidebarMain/>
    <ContainerMain/>
    <FooterMain/>
    <!-- <MenuMain/> -->
  </div>
  
</template>

<script>

import ContainerMain from './components/ContainerMain.vue';
import FooterMain from './components/FooterMain.vue';
import SidebarMain from './components/SidebarMain.vue';

// import MenuMain from './components/MenuMain.vue';


export default {
  name: 'App',
  components: {
    ContainerMain,
    FooterMain,
    SidebarMain,
    // MenuMain,
  },
  data () {
    return {
      dark_theme: true,
      open_options: false,
      view:1,
    
    }
  },
  watch:{
      dark_theme(newTheme, oldTheme) {
        if (newTheme == true && oldTheme ==false) {
          document.body.style.backgroundColor = "#363634"; 
        }else{
          document.body.style.backgroundColor = "#ffffff";
          
        }
      }
  },
  created(){
    
  },
  
}
</script>

<style scoped>
  @import "./assets/css/main.css";
</style>
