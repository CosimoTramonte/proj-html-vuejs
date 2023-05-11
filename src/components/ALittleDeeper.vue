
<script>
import ALittleDeeperCard from "./partials/ALittleDeeperCard.vue"
import {CardALittleDeeper} from "../data/data"

export default {
    name:"ALittleDeeper",
    components:{
        ALittleDeeperCard
    },
    data(){
        return{
            CardALittleDeeper
        }
    }
}
</script>

<template>

    <section>
        <h2>Dig A Little Deeper Into Damon Vaughn</h2>
        <h4>FIND OUT MORE ABOUT THE AUTHOR HIMSELF</h4>

        <div class="containerCard">

            <ALittleDeeperCard
            v-for="(card,index) in CardALittleDeeper" :key="index"
                :image="card.image"
                :title="card.title"
                :description="card.description"
            />

        </div>


    </section>
  
</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    section{
        text-align: center;
        padding: 5%;

        h2{
            font-size: 40px;
            font-family: "DM Serif Display",serif;
            padding-bottom: 1%;
        }

        h4{
            font-size: 18px;
            font-family: "DM Sans", Arial, Helvetica, sans-serif;
            color: #49A987;
            letter-spacing: 1px;
            padding-bottom: 50px;
        }

        .containerCard{
            display: flex;
            justify-content: space-around;
            align-items: flex-start;
        }
    }

</style>