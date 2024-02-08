<template>
  <div class="sidebar-container">
    <div v-for="(option, index) in options" :key="index" class="sidebar-option" @click="scrollIndex(index)">
        <svg  v-if="option.page==1" class="feather feather-home" fill="none" height="24" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
        <svg  v-if="option.page==3" class="feather feather-award" fill="none" height="24" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><circle cx="12" cy="8" r="7"/><polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"/></svg>
        <!-- <svg  v-if="option.page==5" class="feather feather-book-open" fill="none" height="24" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"/><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg> -->
        <svg  v-if="option.page==6" class="feather feather-message-square" fill="none" height="24" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
    </div>
    <div class="theme-switch-margin">
    </div>

    <div class="option-button switch">
      <label class="theme-switch">
        <input type="checkbox" v-model="$parent.dark_theme">
        <span class="theme-slider"></span>
      </label>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'SidebarMain',
  props: {
    
  },
  data(){
    return{
      options:[
              {
                name:'Introduction',
                icon:'init.png',
                page:1
              },
              {
                name:'Skills',
                icon:'skills.png',
                page:3
              },
              
              // {
              //   name:'Knowledge',
              //   icon:'knowledge.png',
              //   page:5
              // },
              {
                name:'Contact',
                icon:'contact.png',
                page:6
              }
              
            ]
    }
    
  },
  methods:{
    scrollIndex(index){
      if(index==0){
        document.getElementById("init-container").scrollIntoView();
      }
      else if(index==1){
        document.getElementById("skills-container").scrollIntoView();
      }
      // else if(index==2){
      //   document.getElementById("init-container").scrollIntoView();
      // }
      else if(index==2){
        document.getElementById("contact-container").scrollIntoView();
      }
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import "../assets/css/sidebar.css";
  @import "../assets/css/options.css";
</style>