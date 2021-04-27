<template>
    <nav>
    <div class="GT">
      <a class="permarker" href="/">Galand Tristan</a>
    </div>
    <div>
      <router-link to="/">Accueil</router-link>
      <router-link to="/cv">CV</router-link>
      <router-link to="/portfolio">Portfolio</router-link>
      <router-link to="/contact">Me Contacter</router-link>
    </div>
  </nav>
  
</template>

<style scoped>
nav {
  margin: 0;
  padding: 30px;
  background: rgba(235, 92, 39, 1);
  display: flex;
  justify-content: space-between;
}
nav a {
  font-weight: bold;
  color: #ffffff;
  padding-left: 20px;
  text-decoration: none;
}
nav a.router-link-exact-active {
  text-decoration:underline;
}
@media (max-width: 800px){
  nav{
    display: flex;
    flex-direction: column;
    padding: 30px 0;
    text-align: center;
  }
  .GT{
    margin-bottom: 20px;
  }
}
</style>