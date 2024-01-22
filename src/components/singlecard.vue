<script>
export default{
    data(){
        return{
        };
    },
    props: {
        card: Object
    }
}
</script>

<template>
    <div class="singlecard">
        <div>
            <img :src="card.thumb" :alt="card.series">
        </div>
        <h5>
            {{ card.series }}
        </h5>
    </div>
</template>

<style lang="scss" scoped>
    .singlecard{
            width: calc(100% / 6);
            padding: 20px;
            text-align: center;
            

            >div{
                margin-bottom: 10px;
            }

            h5{
                text-transform: uppercase;
                color: white;
            }
        }

</style>