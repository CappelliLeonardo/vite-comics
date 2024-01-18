<script>
export default {
    data() {
        return {
            nav:[
                
                {
                    name: 'CHARACTERS',
                    link: '#nogo'
                },
                {
                    name: 'COMICS',
                    link: '#nogo'
                },
                {
                    name: 'MOVIES',
                    link: '#nogo'
                },
                {
                    name: 'TV',
                    link: '#nogo'
                },
                {
                    name: 'GAMES',
                    link: '#nogo'
                },
                {
                    name: 'COLLECTIBLES',
                    link: '#nogo'
                },
                {
                    name: 'VIDEOS',
                    link: '#nogo'
                },
                {
                    name: 'FANS',
                    link: '#nogo'
                },
                {
                    name: 'NEWS',
                    link: '#nogo'
                },
                {
                    name: 'SHOP',
                    link: '#nogo'
                },
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
    <header>
        <div class="main-container">
            <!-- contenitore IMG -->
            <div>
                <img src="../assets/vue.svg" alt="">
            </div>
            <!-- navbar -->
            <ul>
                <li v-for="(elem , i) in nav" :key="i">
                    {{ elem.name }}
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
   @use "../assets/scss/partials/mixins.scss" as *;
   .main-container{
    @include main-container;
   }
</style>
