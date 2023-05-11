
<script>
export default {
    name:"ALittleDeeperCard",
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
            <div class="wrapper">
                <img :src="getImage(image)" alt="A Little Deeper Img">
            </div>
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
        max-height: 650px;
        aspect-ratio: 2/3;
        width: 28%;
        position: relative;
        border-end-end-radius: 100px;
        overflow: hidden;
        transition: all 0.3s;

        &:hover{
            transform: scale(1.05);
            cursor: pointer;
            box-shadow: 0 0 10px 5px rgba(90, 90, 90, 0.219);
        }

        .imgDiv{
            width: 100%;
            height: 100%;

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
                filter: brightness(0.8);
            }
        }

        .infoDiv{
            position: absolute;
            margin-left: auto;
            margin-right: auto;
            left: 0;
            right: 0;
            bottom: 15%;
            text-align: center;

            h3{
                font-family: "DM Sans", Arial, Helvetica, sans-serif;
                font-size: 26px;
                color: white;
            }

            hr{
                width: 30%;
                margin: 0 auto;
                color: white;
            }

            p{
                color: $primary-color;
                line-height: 30px;
                font-weight: 400;
                font-family: "DM Sans", Arial, Helvetica, sans-serif;
                font-size: 18px;
            }
        }
    }

</style>