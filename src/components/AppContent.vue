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

<div class="container">
    <div class="row">

       <AppCard  v-for="(item3, index3) in card_dc" :card_dc= "item3" :poster="image-poster" />
   </div>
</div>


</main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {

    background-color: black;
    padding: $paddingSemantic;
    color: white;
}


.container {}

.row {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
}
</style>