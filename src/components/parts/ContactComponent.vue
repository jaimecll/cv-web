<template>
  <div class="part-container contact-container" id="contact-container">
    <div  class="contact-info">
      <h1>Contact me</h1>
      <p>You can <span>contact me</span> directly here</p>
      <br><br>
      <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
        <path stroke="currentColor" stroke-linecap="round" stroke-width="2" d="m3.5 5.5 7.9 6c.4.3.8.3 1.2 0l7.9-6M4 19h16c.6 0 1-.4 1-1V6c0-.6-.4-1-1-1H4a1 1 0 0 0-1 1v12c0 .6.4 1 1 1Z"/>
      </svg>
      <p>jaimecgfg@gmail.com</p>
      <br>
      <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 13a3 3 0 1 0 0-6 3 3 0 0 0 0 6Z"/>
        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.8 14h0a7 7 0 1 0-11.5 0h0l.1.3.3.3L12 21l5.1-6.2.6-.7.1-.2Z"/>
      </svg>
      <p>Barcelona - Spain</p>
      <br>
      <img>
      <img>
    </div>
    <div id="contact-form">
                <form
                  action="https://formspree.io/f/mkndjyad"
                  method="POST"
                  class="contact-form"
                  v-on:submit="validateForm()"
                >
                <div class="col-full">
                  <label class="form-label">
                    Email:
                  </label>
                  <input id="email-input" class="form-input" type="email" name="Email" placeholder="Email">
                </div>
                <div class="col-full">
                  <label class="form-label">
                    Subject:
                  </label>
                  <input id="subject-input" class="form-input" type="text" name="Subject" placeholder="Name">
                </div>
                  
                <div class="col-full">
                  <label class="form-label">
                    Message:
                  </label>
                  <textarea id="message-input" class="form-input" name="Message" placeholder="Message"></textarea>
                  
                  <!-- your other form fields go here -->
                  <button type="submit" >Send</button>
                </div>
                </form>
        </div>
  </div>
</template>

<script>
export default {
  name: 'ContactComponent',
  props: {
    
  },
  
  methods:{
    validateForm(){
      
       
      let boolean=true;
      let email = document.getElementById("email-input");
      let subject = document.getElementById("subject-input");
      let message = document.getElementById("message-input");
      if(email.value==""){
        email.classList.add("input-error");
        boolean=false;
      }else{
        email.classList.remove("input-error");
      }
      if(subject.value==""){
        subject.classList.add("input-error");
        boolean=false;
      }else{
        subject.classList.remove("input-error");
      }
      if(message.value==""){
        message.classList.add("input-error");
        boolean=false;
      }else{
        message.classList.remove("input-error");
      }
      if(!boolean){
        
         event.preventDefault();
      }else{
        return true;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import "../../assets/css/parts/contact.css";
</style>