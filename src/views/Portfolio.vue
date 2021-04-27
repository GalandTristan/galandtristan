<template>
  <div class="portfolio">
    <h1>Portfolio</h1>
    <div class="fiche">
      <template :key="index" v-for="(projet, index) in projets">
      <div class="ficheart">
        <Realisation :titre="projet.nom" :image="projet.img" :description="projet.info" :bouton="projet.lien"/>
      </div>
    </template>
    </div>
  </div>
</template>

<script>
import Realisation from "@/components/Realisation"
export default {
  components:{
    Realisation
  },
  data(){
    return{
      projets:[
        {
          nom:"VisualKraken",img:"https://api.galandtristan.be/uploads/mockup_VK_46f786e0ff.png",info:"VisualKraken propose nos service de création de site web, de graphisme et de communication via les réseaux sociaux ou vidéo.", lien:"https://visualkraken.netlify.app/"
        },
        {
          nom:"Lorem Ipsum",img:"https://api.galandtristan.be/uploads/Mockup_mac_bec9c682df.webp",info:"À force d'utiliser les outils gratuits en ligne, nous avons décidé, avec Benjamin Geets, de développer notre propre générateur de texte Lorem Ipsum.", lien:"https://lachougle.be/"
        },
        {
          nom:"ConsommerTournai",img:"https://api.galandtristan.be/uploads/Mockup_Consommer_Tournai_2edaa17784.webp",info:"Cette plateforme avait vocation à mettre en avant si les différents commerces tournaisiens étaient ouverts, fermés, s'ils faisaient du click 'n collect, ...", lien:"https://lachougle.be/"
        },
        {
          nom:"Bertrand's Quest",img:"https://api.galandtristan.be/uploads/boss_87d009b397.svg",info:"Création des personnages et décors d'un jeu pensé, conçu et développé en 24h lors des Space Office Hackaton 2021 organisé par le MIC.", lien:"https://lachougle.be/"
        },
        {
          nom:"Site Personnel",img:"https://api.galandtristan.be/uploads/illu_site_1a1e4b17c3.svg",info:"Pour la création de mon site personnel, je me suis occupé de l'identité graphique, des illustrations, web design et du developpement", lien:"https://lachougle.be/"
        },
        {
          nom:"Jardin de Greg",img:"https://geets.dev/img/portfolio/jardingreg.webp",info:"Réalisation du design du site de Ô Jardin de Greg.", lien:"https://jardingreg.be/"
        },
        {
          nom:"La Chougle",img:"https://api.galandtristan.be/uploads/Resposive_Presentation_c11ee1d116.webp",info:"Le site de la Chougle a pour vocation de présenté la bière brassée par le conseil des jeunes d'Amougies.", lien:"https://lachougle.be/"
        }
      ]
    }
  }
}
</script>

<style scoped>
.portfolio{
  margin: 0 25vw;
}

.portfolio p{
  text-align: center;
  font-weight: bold;
  font-size: 36px;
}
.fiche{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

@media (max-width: 800px){
  
}
</style>

réalisation
expérience 
skill