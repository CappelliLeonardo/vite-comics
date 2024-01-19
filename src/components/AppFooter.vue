<script>
export default {
    data() {
        return {
                firstnavs:[
                    {topic:'Characters'},
                    {topic:'Comics'},
                    {topic:'Movies'},
                    {topic:'Tv'},
                    {topic:'Games'},
                    {topic:'Videos'},
                    {topic:'News'}
                ],
                secondnavs:[
                    {topic:'Shop DC'},
                    {topic:'Shop DC Collectibles'}
                ],
                thirdnavs:[
                    {topic:'Terms Of Use'},
                    {topic:'Privacy policy (News)'},
                    {topic:'Ad Choices'},
                    {topic:'Advertising'},
                    {topic:'Jobs'},
                    {topic:'Subscriptions'},
                    {topic:'Talent Workshops'},
                    {topic:'CPSC Certificates'},
                    {topic:'Ratings'},
                    {topic:'Shop Help'},
                    {topic:'Contact Us'},
                ],
                fourthnavs:[
                    {topic:'DC'},
                    {topic:'MAD Magazine'},
                    {topic:'DC Kids'},
                    {topic:'DC Universe'},
                    {topic:'DC Poewer Vista'}

                ],
                socialrefs:[
                    {topic:'../public/img/footer-facebook.png'},
                    {topic:'../public/img/footer-twitter.png'},
                    {topic:'../public/img/footer-youtube.png'},
                    {topic:'../public/img/footer-pinterest.png'},
                    
                ]

        };
    },
    methods: {

    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="main-container">
                <div class="nav-container">
                    <div>
                        <div>
                            <!-- PRIMO NAV -->
                            <h3>DC COMICS</h3>
                            <ul>
                                <li v-for="(elem,i) in firstnavs" :key="i">
                                    <a href="">{{ elem.topic }}</a>
                                </li>
                            </ul>
                        </div>
                        <div>
                            <!-- SECONDO NAV -->
                            <h3>SHOP</h3>
                            <ul>
                                <li v-for="(elem,i) in secondnavs" :key="i">
                                    <a href="">{{ elem.topic }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    
                    <div>
                        <!-- TERZO NAV -->
                        <h3>DC</h3>
                        <ul>
                            <li v-for="(elem,i) in thirdnavs" :key="i">
                                <a href="">{{ elem.topic }}</a>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <!-- QUARTO NAVS -->
                        <h3>SITES</h3>
                        <ul>
                            <li v-for="(elem,i) in fourthnavs" :key="i">
                                <a href="">{{ elem.topic }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="img-dc">
                    <img src="../../public/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="main-container">
                <div>
                    <button>
                        SIGN-UP NOW!
                    </button>
                    <div>
                        <a href="">
                            <h5>FOLLOW US</h5>
                        </a>

                        <ul>
                            <li v-for="(elem,i) in socialrefs" :key="i">
                                <a href="">
                                    <img :src="elem.topic">
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
    @use "../assets/scss/partials/mixins.scss" as *;
   .main-container{
    @include main-container;
    display: flex;
    justify-content: space-between
   }

   .nav-container{
    @include d-flex;
    width:30%;
   }
   .img-dc{
    width: 400px;
    height: 400px;
        img{
            width: 100%;
        }
   }
</style>
