<script>
import AppCard from './AppCard.vue';
import dataItems from '../assets/data/dataItems'

export default {
    components: {
        AppCard

    },
    data() {
        return {

            card_dc: dataItems,

        }
    }
}
</script>

<template lang="">
<main>

<div class="jumbotron">
<button class="btn"><h2>CURRENT SERIES</h2></button>
</div>


<div class="container">
    <div class="row">

       <AppCard  v-for="(item3, index3) in card_dc" :card_dc= "item3" :poster="image-poster" />
   </div>
</div>

<div class="flex">
<button class="btn"><h3>LOAD MORE</h3></button>
</div>



</main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {

    background-color: #1c1c1c;
    color: white;
    position: relative;
}

.container {
    padding: $paddingSemantic;
}

.row {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
}

.btn {
    background-color: $primary;
    padding: 10px 30px;
    border: none;
    color: white;
}

.flex {
    display: flex;
    justify-content: center;
    padding: $paddingSemantic;
}

.jumbotron {
    height: 530px;
    background-image: url("src/assets/images/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;


    .btn {
        position: absolute;
        top: 515px;
        left: 250px;

    }
}
</style>