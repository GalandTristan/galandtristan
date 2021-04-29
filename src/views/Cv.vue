<template>
  <div class="cv">
    <h1>CV</h1>

    <!-- Expérience -->
    <h2>Expérience</h2>
    <template :key="index" v-for="(projet, index) in projets">
      <div class="experience">
        <Experience :titre="projet.nom" :date="projet.date" :description="projet.description"/>
      </div>
    </template>

    <!-- Compétences -->
    <h2>Compétences</h2>
    <div class="logo">
      <template :key="index" v-for="(comp, index) in comps">
        <Skill :image="comp.image"/>
    </template> 
    </div>
  </div>
</template>

<script>
import Experience from "@/components/Experience.vue"
import Skill from "@/components/Skill.vue"
export default {
  components:{
    Experience, Skill
  },
  data(){
    return{
      projets:[
        {
          nom:"Serveur",date:"2015-2020",description:"Pendant plus de 5 ans, j’ai été serveur dans différents restaurants et événements (Comptoir 17, Beffroi, Ferme du Reposoir, Jeudis Oui et Cense de Rigaux)."
        },
        {
          nom:"Vendeur",date:"2020-2021",description:"Je suis vendeur (étudiant) chez JD Sport dans le centre commercial les Bastions."
        },
        {
          nom:"Consultant réseaux sociaux",date:"2021",description:"J’ai apporté mon aide pour lié les réseaux sociaux à la boutique en ligne sur Shopify."
        },
        {
          nom:"Création de Menu",date:"2020-2021",description:"Réalisation de plusieurs menus à l’occasion d’événement tels que la St Valentin, Nouvel An, etc."
        }
      ],
      comps:[
        {
          image:"https://galandtristan.be/media/illustrator.png"
        },
        {
          image:"https://galandtristan.be/media/figma.png"
        },
        {
          image:"https://galandtristan.be/media/aftereffects.png"
        },
        {
          image:"https://galandtristan.be/media/premiere.png"
        },
        {
          image: require("@/assets/logoLogiciels/Ps.png")
        },
        {
          image: require("@/assets/logoLogiciels/Odoo.png")
        },
        {
          image:"https://galandtristan.be/media/office.png"
        },
        {
          image: require("@/assets/logoLogiciels/html5.png")
        },
        {
          image: require("@/assets/logoLogiciels/CSS3.png")
        },
        {
          image: require("@/assets/logoLogiciels/vuejs.png")
        }
      ]
    }
  }
}
</script>

<style scoped>
.cv{
  margin: 20px 500px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.cv p{
  height: 70vh;
  text-align: center;
  font-weight: bold;
  font-size: 36px;
}
.cv div{
  margin: 10px 0;
}
.cv .logo{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.cv img{
  height: 60px;
  width: 60px;
  margin: 20px;
}
.cv h2{
  margin: 20px 0;
}
@media (max-width: 1500px){
  .cv{
    margin: 20px 15px;
    justify-content: left;
  }
  .experience{
    padding :10px;
  }
}

</style>