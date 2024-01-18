<script>
export default {
    data() {
        return {
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
    methods: {

    }
}
</script>

<template>
    <main>
        <div class="main-container">
            <h1>
                Content goes here
            </h1>
        </div>
        <div class="main-container bluecolor">
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
    </main>
</template>

<style lang="scss" scoped>
    @use "../assets/scss/partials/mixins.scss" as *;
    @use "../assets/scss/partials/variables.scss" as *;

   .main-container{
    @include main-container;
    background-color: $brand_primary;
   }

   .bluecolor{
    background-color:#4882F9;
    display: flex;
    justify-content: center;
}

.img-container-item{
    width: 50px;
    height: 50px;
}
img{
    width: 100%;
    object-fit: contain;
    height: 100%;
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
   
</style>
