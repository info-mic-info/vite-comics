<script>
import AppCard from './AppCard.vue';
import dataItems from '../assets/data/dc-comics.json;'

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
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure totam magnam perspiciatis quis magni, deserunt distinctio explicabo saepe iste, neque sequi sit! Rerum dignissimos, nisi commodi incidunt corrupti ducimus fuga. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quod officia voluptatum provident, iste nihil at officiis nisi unde asperiores facere sit incidunt mollitia magnam enim suscipit harum commodi distinctio. Laborum. </p>

  <AppCard />
  <AppCard />

</main>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {

    background-color: black;
    height: 200px;
    padding: $paddingSemantic;
    color: white;
}
</style>