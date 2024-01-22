<script>
import logo from '../assets/img/dc-logo.png'
export default {
    data() {
        return {
            logo,
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
            <div class="img-container">
                <img :src="logo" alt="">
            </div>
            <!-- navbar -->
            <ul class="d-flex">
                <li class="list" v-for="(elem , i) in nav" :key="i">
                    <a href="http://">
                        {{ elem.name }}
                    </a>
                
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
   @use "../assets/scss/partials/mixins.scss" as *;
   @use "../assets/scss/partials/variables.scss" as *;


   .main-container{
    @include main-container;
    @include d-flex;
    align-items: center;
   }

   .list{
    margin: 10px;
   }
   a{
    color: $brand_primary;
    font-weight: bold;
        &:hover{
            color: #1161F9;
        }
   }

   .d-flex{
    @include d-flex;
   }
</style>
