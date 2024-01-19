<script>

import singlecard from './singlecard.vue';
export default {
    data() {
        return {
        cards:[
            {
                "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book",
            },
            {
                "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book",
            },
            {
                "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel",
            },
            {
                "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book",
            },
            {
                "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book",
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel",
            },
            ],

            itemsLink: [
                    {
                        img: '../public/img/buy-comics-digital-comics.png',
                        name: 'DIGITAL COMICS',
                        link: '',
                    },
                    {
                        img: '../public/img/buy-comics-merchandise.png',
                        name: 'DC MERCHANDISE',
                        link: '',
                    },
                    {
                        img: '../public/img/buy-comics-subscriptions.png',
                        name: 'SUBSCRIPTIONS',
                        link: '',
                    },
                    {
                        img: '../public/img/buy-comics-shop-locator.png',
                        name: 'COMICS SHOP LOCATOR',
                        link: '',
                    },
                    {
                        img: '../public/img/buy-dc-power-visa.svg',
                        name: 'DC POWER VISA',
                        link: '',
                    },
                ],
            
            
        };
    },

    components: {
        singlecard
    },

    methods: {

    }
}
</script>

<template>
    <main>
        <div class="jumbotron">

        </div>
        <div class="bg-color">
            <div class="main-container">
                <h2>
                    CURENT SERIES
                </h2>
                <div class="card-container">
                    <singlecard  
                    v-for="(card,i) in cards" 
                    :key="i"
                    :card="card"
                    />
                </div>
            </div>
        </div>
        
        <div class="bluecolor">
            <div class="main-container">
                <ul>
                    <li v-for="(elem,i) in itemsLink" :key="i">
                        <a :href="elem.link">
                            <div class="img-container-item">
                                <img :src="elem.img" :alt="elem.name">
                            </div>
                            <span>{{elem.name}}</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use "../assets/scss/partials/mixins.scss" as *;
    @use "../assets/scss/partials/variables.scss" as *;

   .main-container{
    @include main-container;
   }
   .bg-color{
    background-color: $brand_primary;

   }

   .bluecolor{
    background-color:#4882F9;
}

.img-container-item{
    width: 50px;
    height: 50px;
}

.card-container{
    display: flex;
    flex-wrap: wrap;
}

.jumbotron{
    background-image: url("/public/img/jumbotron.jpg");
    min-height: 300px;
   
}

ul{
    display: flex;
    align-items: center;
    justify-content: space-between;
    li{
        list-style-type: none;
        
        a{
            display: flex;
            align-items: center;
            color: white;
            text-decoration: none;
            margin-right: 30px;
        }
    }
}

h2{
    padding:50px 10px;
    text-align: left;
    color: white;
}
   
</style>
