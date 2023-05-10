
<script>
export default {
    name: "UpComingCard",
    props:{
        image: String,
        title: String,
        description: String
    },
    methods:{
        getImage(img) {
            return new URL(`../../assets/img/${img}`, import.meta.url).href
        },
    }
}
</script>

<template>

    <div class="ct-card">

        <div class="imgDiv">
            <img :src="getImage(image)" alt="Upcoming Img">
        </div>

        <div class="infoDiv">

            <h3>{{ title }}</h3>
            <hr>
            <p>{{ description }}</p>

        </div>

    </div>
  
</template>

<style lang="scss" scoped>
    @use "../../scss/partials/utilities" as *;
    @use "../../scss/partials/mixin" as *;

    .ct-card{
        width: calc(100% / 3);
        padding: 25px;
        height: 100%;

        .imgDiv{
            width: 100%;

            img{
                width: 100%;
                object-fit: contain;
            }
        }

        .infoDiv{
            background-color: white;
            padding: 35px;
        }

    }


</style>