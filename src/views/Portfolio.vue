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
          nom:"VisualKraken",img:"https://api.galandtristan.be/uploads/medium_Visual_Kraken_57cf859ce1.png",info:"VisualKraken propose nos service de création de site web, de graphisme et de communication via les réseaux sociaux ou vidéo.", lien:"https://visualkraken.netlify.app/"
        },
        {
          nom:"Lorem Ipsum",img:"https://api.galandtristan.be/uploads/medium_miniatiure_lorem_ipsum_c90dc619d7.webp",info:"À force d'utiliser les outils gratuits en ligne, nous avons décidé, avec Benjamin Geets, de développer notre propre générateur de texte Lorem Ipsum.", lien:"https://lorem.geets.dev/"
        },
        {
          nom:"ConsommerTournai",img:"https://api.galandtristan.be/uploads/medium_Consommer_Tournai_5914d03c7d.png",info:"Cette plateforme avait vocation à mettre en avant si les différents commerces tournaisiens étaient ouverts, fermés, s'ils faisaient du click 'n collect, ...", lien:"https://galandtristan.be/portfolio/consommertournai"
        },
        {
          nom:"Bertrand's Quest",img:"https://api.galandtristan.be/uploads/medium_bertrand_s_quest_4a61fc1fc2.webp",info:"Création des personnages et décors d'un jeu pensé, conçu et développé en 24h lors des Space Office Hackaton 2021 organisé par le MIC.", lien:"https://bourgysquest.netlify.app/"
        },
        {
          nom:"Site Personnel",img:"https://api.galandtristan.be/uploads/medium_Illu_site_1_ad37543e9a.webp",info:"Pour la création de mon site personnel, je me suis occupé de l'identité graphique, des illustrations, web design et du developpement", lien:"https://galandtristan.be/"
        },
        {
          nom:"Jardin de Greg",img:"https://api.galandtristan.be/uploads/medium_jardin_de_greg_48a6badc69.webp",info:"Réalisation du design du site de Ô Jardin de Greg.", lien:"https://jardingreg.be/"
        },
        {
          nom:"La Chougle",img:"https://api.galandtristan.be/uploads/medium_La_Chougle_1a1d55ab7a.webp",info:"Le site de la Chougle a pour vocation de présenté la bière brassée par le conseil des jeunes d'Amougies.", lien:"https://lachougle.be/"
        }
      ]
    }
  }
}
</script>

<style scoped>
.portfolio{
  margin: 0 300px;
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
@media (max-width: 1500px){
  .portfolio{
    margin: 0 10px;
  }
}
@media (max-width: 800px){
  .portfolio{
    margin: 0 10px;
  }
}
</style>