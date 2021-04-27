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
          nom:"Serveur",date:"2015-2020",description:"Pendant plus de 5 ans, j’ai été serveur dans différents restaurants et évènement (Comptoir 17, Beffroi, Ferme du Reposoir, Jeudis Oui et Cense de Rigaux)."
        },
        {
          nom:"Vendeur",date:"2020-2021",description:"Je suis vendeur (étudiant) chez JD Sport dans le centre commercial les Bastions."
        },
        {
          nom:"Consultant réseaux sociaux",date:"2021",description:"J’ai apporté mon aide pour lié les réseaux sociaux à la boutique en ligne sur Shopify."
        },
        {
          nom:"Création de Menu",date:"2020-2021",description:"Réalisation de plusieurs menu à l’occasion d’évènement tels que la la St Valentin, Nouvel An, etc."
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
          image:"https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Adobe_Photoshop_CC_icon.svg/1200px-Adobe_Photoshop_CC_icon.svg.png"
        },
        {
          image:"https://lgc.digital/wp-content/uploads/2020/06/Odoo.png"
        },
        {
          image:"https://galandtristan.be/media/office.png"
        },
        {
          image:"http://assets.stickpng.com/thumbs/5847f5bdcef1014c0b5e489c.png"
        },
        {
          image:"https://winieski-k.github.io/assets/img/CSS3.png"
        },
        {
          image:"https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1200px-Vue.js_Logo_2.svg.png"
        }
      ]
    }
  }
}
</script>

<style scoped>
.cv{
  width: 25vw;
  margin: 20px auto;
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
@media (max-width: 800px){
  .cv{
    width: 100vw;
    justify-content: left;
  }
  .experience{
    padding :10px;
  }
}
</style>