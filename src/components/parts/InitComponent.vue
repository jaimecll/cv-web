<template>
  <div class="part-container init-container" id="init-container">
    <div class="init-second-container">
      <h1 class="line-1 animation-typing">Hi, my name is</h1>
      <h2 class="line-1 animation-typing2">Jaime Carcedo</h2>
      <h3 class="line-1 animation-typing3">FullStack Developer</h3>
      
    </div>
    <br><br>
    <div class="user-card">
      <div class="content">
        <div class="column col-40" >
            <img :src="require('@/assets/img/user/user_picture.png')">
        </div>
        <div class="column col-60">
          <div class="column col-100" >
            <h1>Jaime Ismael Carcedo Galindo</h1>
            <p><em><span>Fullstack developer</span></em></p>
            <div class="separator-line"></div>
          </div>
          <div class="column col-100" >
            <p>
              My goal is to grow as a programmer day by day, contributing my knowledge as a web developer. Open to learning new programming languages and methodologies.
              I consider myself an organized person with good teamwork.
              <!-- Como objetivo tengo crecer como programador dia a dia, aportando mis conocimientos como desarrollador web. Abierto a aprender nuevos lenguajes de programación y metodologias.
              Me considero una persona organizada con un buen trabajo en equipo.  -->
              <br><br>
              My main passion for programming is to improve my code to obtain better optimization.
            </p>
          </div>
          
        </div>
        
        
        
      </div>
      <div class="footer">
        <a href="\cv\CV-Jaime_Ismael_Carcedo_Galindo.pdf" download><img :src="require('@/assets/img/logo/pdf.svg')" alt="CV"></a>
        <a href="https://www.linkedin.com/in/jaime-ismael-carcedo-galindo-8724701b7/"><img :src="require('@/assets/img/logo/linkedin.svg')" alt="LinkedIn"></a>
        <a href="https://github.com/jaimecll"><img :src="require('@/assets/img/logo/github.svg')" alt="Github"></a>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "InitComponent",
  props: {},
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../assets/css/parts/aboutme.css";

@import "../../assets/css/parts/init.css";
</style>
