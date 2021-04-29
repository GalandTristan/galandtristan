<template >
    <div class="contenu">
        <img :src="image" class="illustration" alt="image">
        <h3 class="permarker">{{titre}}</h3>
        <p>{{description}}</p>
        <a :href="bouton"><button>Voir <img src="@/assets/linkext.svg" alt="lien ext"></button></a>
    </div>
</template>

<script>
export default {
    props:['titre','image','description','bouton']
}
</script>

<style scoped>
.contenu{
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 20px;
    width: 350px;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    border-radius: 10px;
}
button{
    cursor:pointer;
}
.contenu h3{
    margin: 10px;
    text-align: center;
}
.contenu p{
    margin: 20px 10px;
}
.contenu .illustration{
    width: 350px;
    border-radius: 10px;
}
.contenu a{
    text-decoration: none;
}
.contenu a button{
    margin: 10px auto;
    width: 35%;
    display: flex;
    justify-content: space-between;
}
.contenu a button img{
    height: 15px;
}
@media (max-width: 800px){
  .contenu{
    width: 300px;
  }
  .contenu .illustration{
    width: 300px;
}
}
</style>