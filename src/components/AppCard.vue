<script>
export default {
    props: {
        cards: Object
    }
}
</script>


<template lang="">
    <div>
        <h1>{{cards.name}}</h1>
    </div>
</template>
<style lang="scss">
h1 {
    color: white;
}
</style>