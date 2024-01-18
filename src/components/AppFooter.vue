<script>
export default {
    data() {
        return {

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
                <div>
                    <div>
                        prima ul 
                    </div>
                    <div>
                        seconda ul
                    </div>
                    <div>
                        terza ul
                    </div>
                    <div>
                        quarta ul
                    </div>
                </div>
                    
                
            </div>
        </div>
        <div class="footer-bottom">
            <div class="main-container">

            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
    @use "../assets/scss/partials/mixins.scss" as *;
   .main-container{
    @include main-container;
   }
</style>
