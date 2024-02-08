<template>
  <div class="general-container">
      <InitComponent />
      <SkillsComponent />
      <ContactComponent />

  </div>
</template>

<script>
import InitComponent from './parts/InitComponent.vue';
import SkillsComponent from './parts/SkillsComponent.vue';
import ContactComponent from './parts/ContactComponent.vue';
export default {
  name: 'ContainerMain',
  props: {
    
  },
  components: {
    InitComponent,
    SkillsComponent,
    ContactComponent,
  },
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import "../assets/css/container.css";
</style>