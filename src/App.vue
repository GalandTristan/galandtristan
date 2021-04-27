<template>
  <Menu/>
  <router-view/>
  <Footer/>
</template>

<script>
import Menu from "@/components/Menu.vue"
import Footer from "@/components/Footer.vue"
export default {
  components:{
    Menu,
    Footer
  }
}
</script>

<style>
*{
  font-family: Arial, Helvetica, sans-serif;
  scroll-behavior: smooth;
  margin: 0;
  padding: 0;
}
body{
  overflow-x:hidden
}

@font-face {
  font-family: "Perma";
  src: local("Perma"),
   url(../font/PermanentMarker.ttf) format("truetype");
}
.permarker{
  font-family: "Perma";
  font-size: 30px;
}
h1{
  font-family: "Perma";
  font-size: 70px;
  text-align: center;
}
h2{
  font-family: "Perma";
  font-size: 50px;
  text-align: center;
}
button{
  padding: 10px 35px;
  background: rgba(235, 92, 39, 1);
  text-decoration: none;
  border: none;
  color: #ffffff;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
}
@media (max-width: 800px){
  h1{
    font-size: 40px;
  }
  h2{
    font-size: 30px;
  }
}
</style>
