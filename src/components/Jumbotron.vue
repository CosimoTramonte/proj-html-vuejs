
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Pagination, Navigation, Autoplay } from 'swiper';
import {jumboArticle} from "../data/data"

export default {
    name: "Jumbotron",
    data(){
        return{
            jumboArticle
        }
    },
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination, Navigation, Autoplay],
      };
    },
}
</script>

<template>

    <div class="ct-container">

        <div class="divInfo">

            <div class="info">

                <h1>Damon Vanghn</h1>
                <swiper
                    :slidesPerView="1"
                    :spaceBetween="30"
                    :loop="true"
                    :autoplay="{
                        delay: 2500,
                        disableOnInteraction: false,
                    }"
                    :navigation="false"
                    :modules="modules"
                    class="mySwiper"
                >
                    
                    <swiper-slide v-for="(article,index) in jumboArticle" :key="index">
                        <p>{{ article.article }}</p>
                        <span>{{ article.fonts }}</span>
                    </swiper-slide>

                </swiper>
            </div>

        </div>

        <div class="divLatestBook">

            <div class="cardLatestBook">

                <div class="latestBook">
                    <div class="imgDiv">
                        <img src="../assets/img/book-widget.png" alt="book widget">
                    </div>

                    <div class="lastBookInfo">
                        <h2>Latest Book Release</h2>
                        <h4>D. VAUGHN AUTOBIOGRAPHY</h4>
                        <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus.</p>
                    </div>
                </div>

                <div class="buyLatestBook">
                    <div class="col buttonDiv1">
                        <button><i class="fa-brands fa-amazon"></i> Buy On Amazon</button>
                    </div>
                    <div class="col buttonDiv2">
                        <button><i class="fa-brands fa-apple"></i> Buy On App Store</button>
                    </div>
                </div>

            </div>


        </div>

    </div>

</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    .ct-container{
        height: calc(100% - 90px);
        padding-left: 11%;
        display: flex;
        justify-content: space-between;


        .divInfo{
            width: 50%;
            height: 100%;
            display: flex;
            justify-content: center;
            flex-direction: column;
            padding-right: 20px;

            .info{

                h1{
                    font-family: Kristi,serif;
                    color: $primary-color;
                    font-size: 90px;
                }

                p{
                    font-family: "DM Serif Display",serif;
                    color: $white-text;
                    font-size: 46px;
                }

                span{
                    color: #A3A1A1;
                    font-size: 25px;
                }
            }

            .nextPrevDiv{
                padding-top: 50px;
                display: flex;
                align-items: flex-start;
                width: 100%;

                button{
                    margin: 0 10px;
                    padding: 5px 10px;
                    background-color: rgba(0, 0, 0, 0.63);
                    color: white;
                    border: 1px solid black;
                    border-radius: 10px;
                }
            }
        }

        .divLatestBook{
            width: 46%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            align-items: flex-end;

            .cardLatestBook{
                background-color: white;
                padding: 5%;
                max-width: 890px;

                .latestBook{
                    display: flex;

                    .lastBookInfo{
                        h2{
                            font-size: 30px;
                            padding: 30px 0 10px;
                            font-family: "DM Serif Display",serif;
                        }

                        h4{
                            color: $primary-color;
                            font-size: 18px;
                            font-family: "DM Serif Display",serif;
                        }

                        p{
                            color: $text-primary-color;
                            font-size: 16px;
                            padding: 10px 0;
                        }
                    }
                }

                .buyLatestBook{
                    display: flex;
                    
                    .buttonDiv1,.buttonDiv2{

                        height: auto;
                        button{
                            width: 90%;
                            padding: 8px 10px;
                            background-color: #F4FAF8;
                            border: 1px solid #49A987;
                            border-radius: 10px;

                            &:hover{
                                background-color:#49A987;
                                color: white;
                            }
                        }

                    }
                }
                
            }

        }
    }
</style>