<template>
  <!-- Heading -->
  <div class="home">
    <img alt="illustration" src="https://galandtristan.be/media/bureau.svg">
  </div>

  <!-- Introduction -->
  <div class="intro">
    <p>Je m’appelle <span id="vert">Galand Tristan</span>,<br> Je suis <span id="rouge">étudiant</span> en <span id="bleu">e-business</span> et passionné par le <span id="jaune">graphisme</span> et le <span id="vertfonce">Web design</span>. </p>
  </div>

  <!-- Réalisations -->
  <div class="realisations">
    <h2>Réalisations</h2>
    <div class="fiche">
      <template :key="index" v-for="(projet, index) in projets">
        <div class="ficheart">
          <Realisation :titre="projet.nom" :image="projet.img" :description="projet.info" :bouton="projet.lien"/>
        </div>
      </template>
    </div>
    <router-link to="/portfolio" class="buttom"> Plus d’illustrations </router-link>
  </div>

  <!-- Informations-->
  <div class="citation bg-custom-citation">
    <p>
      Depuis maintenant plusieurs année, ce qui me fait vibrer c’est le design.
      Que ça soit pour la réalisation d’une identité graphique, d’une carte de restaurant ou bien du design d’un site web, chaque projet confirme mon envie de faire de cette passion mon métier.
    </p>
    <h3>Compétences : </h3>
    <div class="logo">
      <template :key="index" v-for="(comp, index) in comps">
        <Skill :image="comp.image"/>
      </template> 
    </div>
    <div>
      <router-link to="/cv" ><img alt="plus" src="@/assets/plus.svg"></router-link>
    </div>
    
  </div>

  <!-- Contact -->
  <div class="contact">
    <router-link to="/contact" ><img alt="illustration" src="https://galandtristan.be/media/contact.svg"></router-link>
  </div>
</template>

<script>
import Realisation from "@/components/Realisation"
import Skill from "@/components/Skill.vue"
export default {
  components:{
    Realisation, Skill
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
        }
      ]
    }
  }
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
}
.home{
  height: 80vh;
  padding: 30px;
  background: rgba(235, 92, 39, 1);
  text-align: center;
}
.home img{
  width: 70vw;
  height: 70vh;
}
.intro{
  margin: 20%;
  text-align: center;
  font-size: 60px;
  font-weight: bold;
}
#vert{
  color: rgba(58, 170, 53, 1);
}
#rouge{
  color: #FF2E00;
}
#bleu{
  color: #2463AA;
}
#jaune{
  color: #FF9F00;
}
#vertfonce{
  color: #235126;
}
.realisations{
  text-align: center;
  padding-bottom: 50px;
}
.realisations .fiche{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 25px 0;
}
.buttom{
  padding: 10px 35px;
  background: rgba(235, 92, 39, 1);
  text-decoration: none;
  border: none;
  color: #ffffff;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
}
.citation{
  height: 50vh;
  padding: 200px 160px;
  margin: 150px 100px;
}
.citation p{
  color: white;
  font-size: 40px;
  text-align: center;
  font-weight: bold;
  line-height: 63px;
}
.citation h3{
  color: white;
  font-size: 45px;
  text-align: center;
  margin: 25px;
  font-family: "Perma";
}
.citation ul{
  color: white;
  font-size: 35px;
  padding-left: 15em;
  list-style:none;
}
.citation div{
  display: flex;
  justify-content: center;
}
.citation div img{
  height: 50px;
  margin: 20px;
}
.bg-custom-citation {
    background: url(https://galandtristan.be/media/hard_work.webp);
    background-size: cover;
    background-repeat: no-repeat;
}
.contact{
  margin:100px;
  display: flex;
  justify-content: center;
}
.contact img{
  width: 70vw;
  height: 70vh;
}
@media (max-width: 800px){
  .home{
    padding: 0;
  }
  .home img{
  width: 100vw;
  height: 70vh;
}
  .intro{
    margin: 30% 10%;
    font-size: 30px;
  }
  .citation{
    padding: 50px 10px;
    margin: 0px;
  }
  .citation p{
    padding: 10px 20px;
    font-size: 18px;
    line-height: initial;
  }
  .citation h3{
    font-size: 25px;
    margin: 10px;
  }
  .citation div img{
    margin: 10px;
  }
  .contact{
    display: flex;
    justify-content: center;
  }
  .contact img{
    
    margin: 0px;
    padding: 0 10px;
    height: auto;
  }
  .contenu{
    margin: 0px;
  }
  .ficheart{
    margin: 20px 0;
  }
}
</style>


