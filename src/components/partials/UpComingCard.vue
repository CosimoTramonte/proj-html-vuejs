
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
            
            &:hover{
                img{
                    filter:brightness(1.25);
                    filter: hue-rotate(20deg);
                    filter: opacity(90%);
                    cursor: pointer;
                }
            }
            
            img{
                width: 100%;
                object-fit: contain;
                transition: all 0.4s;
            }
        }

        .infoDiv{
            background-color: white;
            padding: 35px;
            
            h3{
                font-family: "DM Sans", Arial, Helvetica, sans-serif;
                font-size: 26px;
                transition: all 0.3s;

                &:hover{
                    color: $primary-color;
                    cursor: pointer;
                }
            }

            p{
                color: #737A82;
                line-height: 30px;
                padding: 0 20px;
                font-weight: 400;
                font-family: "DM Sans", Arial, Helvetica, sans-serif;
                font-size: 18px;
            }
        }

    }


</style>