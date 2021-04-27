<template >
    
        <div class="xp">
            <h3>{{titre}}</h3>
            <p>{{date}}</p>
        </div>
        <p>{{description}}</p>
</template>

<script>
export default {
    props:['titre','date','description']
}
</script>

<style scoped>
.xp{
    display: flex;
    align-items: flex-end;
}
.xp p{
    color: grey;
    margin: 0 10px;
}
p{
    margin-top: 10px;
}
@media (max-width: 800px){

    .xp h3{
        width: initial;
    }
    p{
        width: 90vw;
    }
}
</style>