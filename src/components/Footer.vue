<template>
    <footer>
    <a href="https://galandtristan.be/">Mon vrai site</a>
    <p>2021 - Galand Tristan</p>
    <img @click="goTop()" src="@/assets/gotop.svg" alt="">

  </footer>
</template>

<script>
export default {
  methods:{
    goTop(){
      window.scrollTo(0,0)
    }
  }
}
</script>

<style scoped>
footer{
  background-color: rgba(235, 92, 39, 1);
  display: flex;
  justify-content: space-around;
  padding: 10px;
  color: #ffffff;
}
footer a{
  color: #ffffff;
  text-decoration: none;
  margin: auto 0;
}
footer p{
  font-family: "Perma";
  font-size: 30px;
}
footer svg{
  margin: auto 0;
}
@media (max-width: 800px){
  footer{
    flex-direction: column;
    text-align: center;
  }
  footer img{
    width: 30px;
    margin: 0 auto;
  }
}
</style>