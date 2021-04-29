<template>
  <div class="about">
    <h1>Me contacter</h1>
    <ButtonMail/>
    <div class="rs">

      <!-- Linkedin -->
      <a href="https://www.linkedin.com/in/galandtristan/">
        <img src="@/assets/linkedin.svg" alt="logo LinkedIn">
      </a>

      <!-- Behance -->
      <a href="https://www.behance.net/galandtristan">
        <img src="@/assets/behance.svg" alt="logo Behance">
      </a>

      <!-- Instagram -->
      <a href="https://www.instagram.com/galandtristan/">
        <img src="@/assets/insta.svg" alt="logo Instagram">
      </a>

      <!-- Twitter -->
      <a href="https://twitter.com/GalandTristan">
        <img src="@/assets/twitter.svg" alt="logo Twitter">
      </a>

      <!-- Youtube -->
      <a href="https://www.youtube.com/channel/UCeGKezysemoQKs8b3dV8iQQ">
        <img src="@/assets/youtube.svg" alt="logo YouTube">
      </a>
    </div>

    <div>
      <img src="@/assets/pcdeface.svg" alt="Image de mon bureau de face">
    </div>
  </div>
</template>
<script>
import ButtonMail from "@/components/ButtonMail.vue"
export default {
  components:{
    ButtonMail
  }
}
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }
  .about{
    background-color: rgba(235, 92, 39, 1);
    text-align: center;
    color: white;
  }
  
  div p{
    font-size: 36px;
    font-weight: bold;
    margin: 50px;
  }
  div .rs{
    margin: 20px;
  }
  div .rs a{
    margin: 20px 20px;
  }
  div img{
    margin: 20px;
  }
  @media (max-width: 800px){
  div p{
    font-size: 25px;
  }
  div .rs{
    margin: 10px;
  }
  div .rs a{
    margin: 10px;
  }
  div img{
    margin: 10px 0;
    width: 100vw;
  }
}
</style>