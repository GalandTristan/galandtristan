<template>
<a :href="mail">
    <button @click="setText()">
        {{textBouton}}
    </button>
</a>
    
    
</template>
<script>
export default{
    data(){
        return{
            textBouton: "Mon mail",mail:"#"
        }
    },
    methods:{
        setText(){
            this.textBouton = "galand.tristan@gmail.com"
            this.mail= "mailto:galand.tristan@gmail.com"
        }
    }
}
</script>

<style scoped>
button{
    cursor:pointer;
    margin: 30px;
    padding:15px 40px;
    background-color: white;
    color: rgba(235, 92, 39, 1);
    font-size: 20px;
}
</style>