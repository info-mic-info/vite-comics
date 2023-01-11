<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    label: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    label: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    label: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    label: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    label: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    label: 'NEWS',
                    url: '#',
                    active: false
                },
                {
                    label: 'SHOP',
                    url: '#',
                    active: false
                },
            ]
        }
    }
}
</script>

<template lang="">

<header>
    <a href="/" class="brand">
        <img src="../assets/images/dc-logo.png" alt="">
    </a>
    <nav>
        <ul>
            <li v-for="(elem, index) in menu" :key="index">

                <a :href="elem.url" :class="elem.active ? 'active' : ''">{{elem.label}}</a>

        </li>
        </ul> 
    </nav>
</header>

</template> 

<style lang="scss">

</style>