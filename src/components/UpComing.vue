
<script>
import UpComingCard from "./partials/UpComingCard.vue"
import {CardUpComing} from "../data/data"

export default {
    name: "UpComing",
    components:{
        UpComingCard
    },
    data(){
        return{
            CardUpComing
        }
    }
}
</script>

<template>

    <section>
        <h2>Upcoming Events</h2>
        <h4>MEET THE AUTHOR IN PERSON</h4>

        <div class="containerCard">

            <UpComingCard
                v-for="(card,index) in CardUpComing" :key="index"
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
        background-color: #FEF7E9;
        padding: 5%;

        h2{
            font-size: 40px;
            font-family: "DM Serif Display",serif;
            padding-bottom: 1%;
        }

        h4{
            font-size: 18px;
            font-family: "DM Sans", Arial, Helvetica, sans-serif;
            color: $primary-color;
        }

        .containerCard{
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
        }
    }



</style>