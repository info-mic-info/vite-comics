<script>
export default {
    props: {
        card_dc: Object
    }
}
</script>


<template lang="">
    <div class="card" >
        
        <img :src=card_dc.thumb alt="">
        <h3>{{card_dc.series}}</h3>
      
    </div>
</template>
<style lang="scss">
h1 {
    color: white;
}

.card {
    margin: 10px 0;
    width: calc(100% / 6);
    text-align: center;

    img {
        width: 300px;
        height: 300px;
    }

}
</style>