<template>
  <div class="part-container skills-container" id="skills-container">


    <div class="knowledge-box">
      <h1>Education:</h1>
      <li>Jesuites bellvitge - Joan XXIII</li>
      <p><em>FP Web Application Development</em></p>
      <p><em>2018-2020</em></p>
      <h1>Experience:</h1>
      <li>Acceleralia</li>
      <p><em>Fullstack developer</em></p>
      <p><em>2020-223</em></p>
    </div>


    <div class="tech-stack-box">
      <h1>Tech stack:</h1>
      <div v-for="(skill, indexSkill) in skills" :key="indexSkill" class="logo-stack-container">
        <img class="logo-stack" :src="skill.image">
      </div>
    </div>


    
    
  </div>
</template>

<script>
export default {
  name: 'SkillsComponent',
  props: {
    
  },
  data(){
    return{
      containerScroll:0,
      skills:[
              {
                name:'HTML',
                percent:'90',
                image:require("@/assets/img/logo/html5.png"),
              },
              {
                name:'CSS',
                percent:'80',
                image:require("@/assets/img/logo/css.png"),
              },
              {
                name:'JavaScript',
                percent:'80',
                image:require("@/assets/img/logo/js.png"),
              },
              {
                name:'JQuery',
                percent:'80',
                image:require("@/assets/img/logo/JQuery.png"),
              },
              {
                name:'MySQL',
                percent:'80',
                image:require("@/assets/img/logo/MySQL.png"),
              },
              
              {
                name:'PHP',
                percent:'100',
                image:require("@/assets/img/logo/php.png"),
              },
              {
                name:'Laravel',
                percent:'70',
                image:require("@/assets/img/logo/laravel.png"),
              },
              
              
              {
                name:'VUE',
                percent:'70',
                image:require("@/assets/img/logo/vue.png"),
              },
              {
                name:'Angular',
                percent:'50',
                image:require("@/assets/img/logo/angular.png"),
              },
              {
                name:'Java',
                percent:'60',
                image:require("@/assets/img/logo/java.png"),
              },
              // {
              //   name:'Git',
              //   percent:'70',
              //   image:require("@/assets/img/logo/git.png"),
              // },
              ]
    }
  },
  methods: {
    prevSlide(){
      this.containerScroll=this.containerScroll - 292;
      if(this.containerScroll<0){
        this.containerScroll=0;
      }
       let container = document.getElementById("skill-cards-container");
       container.scrollTo({left: this.containerScroll, behavior: 'smooth'})
      //  container.scrollLeft= container.scrollLeft - 876;
    },
    nextSlide(){
      
      this.containerScroll=this.containerScroll + 292;
       let container = document.getElementById("skill-cards-container");
       console.log(container.scrollWidth);
      if(this.containerScroll>container.scrollWidth - 876){
        this.containerScroll = container.scrollWidth - 876;
      }

       container.scrollTo({left: this.containerScroll, behavior: 'smooth'})
      //  container.scrollLeft= container.scrollLeft + 876;
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../assets/css/parts/skills.css";
</style>