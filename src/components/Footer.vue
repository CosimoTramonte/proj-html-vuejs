
<script>
import {FooterMenu} from "../data/data"

export default {
    name:"Footer",
    data(){
        return{
            FooterMenu
        }
    },
}
</script>

<template>

    <footer>

        <div class="main-wrapper">

            <div class="footerSuperiorDiv">
    
                <div class="logoDiv">
                    <img src="../assets/img/author-logo-round.png" alt="logo author">
                </div>

                <div class="aboutMeDiv">
                    <h3>ABOUT ME</h3>
                    <p>{{ FooterMenu.aboutMe }}</p>
                </div>

                <div class="usefulLinksDiv">
                    <h3>USEFUL LINKS</h3>
                    <ul>
                        <li v-for="(link,index) in FooterMenu.useFulLinks" :key="index"><a href="#">{{ link.text }}</a></li>
                    </ul>
                </div>

                <div class="contactInfoDiv">
                    <h3>CONTACT INFO</h3>
                    <ul>
                        <li v-for="(link,index) in FooterMenu.contactInfo" :key="index" v-html="link.text"></li>
                    </ul>
                    <ul class="socialUl">
                        <li v-for="(social,index) in FooterMenu.soiclaContact" :key="index" class="social"><i :class="social"></i></li>
                    </ul>
                </div>
    
            </div>
    
            <div class="footerInferiorDiv">
                <p>© Copyright 2012 - 2023 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
            </div>

        </div>

    </footer>
  
</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    footer{
        width: 100vw;
        background-image: url("../assets/img/hero-07-2x.jpg");
        background-repeat: no-repeat;
        background-size: cover; 
        background-position: top;

        .main-wrapper{
            width: 100%;
            height: 100%;
            background: linear-gradient( rgba(0, 0, 0, 0.3),  rgba(0, 0, 0, 0.945));
            padding: 8% 6% 6%;

            .footerSuperiorDiv{
                @include centerFlex("both");
                align-items: stretch;
                justify-content: space-between;

                h3{
                    color: white;
                    font-family: "DM Serif Display", serif;
                }


                .logoDiv{
                    width: 15%;
                    img{
                        width: 100%;
                        object-fit: contain;
                    }
                }

                .aboutMeDiv{
                    color: #CCCCCC;
                    margin: 0 2%;
                    width: 20%;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;

                    h3{
                        padding-bottom: 40px;
                    }
                }

                .usefulLinksDiv{
                    width: 25%;

                    h3{
                        padding-bottom: 30px;
                    }

                    ul{
                        list-style: none;
                        font-family: "DM Sans", Arial, Helvetica, sans-serif;

                        li{
                            color: white;
                            padding: 5px 0;
                            font-weight: 800;

                            &::before{
                                content: ">";
                                padding-right: 10px;
                            }

                            a{
                                text-decoration: none;
                                color: #CCCCCC;
                                font-weight: 400;

                                &:hover{
                                    color: $primary-color;
                                }
                            }

                        }
                    }

                }

                .contactInfoDiv{
                    width: 35%;

                    h3{
                        padding-bottom: 30px;
                    }

                    ul{
                        list-style: none;
                        font-family: "DM Sans", Arial, Helvetica, sans-serif;

                        li{
                            padding: 5px 0;
                            color: #CCCCCC;
                        }
                    }

                    .socialUl{
                        list-style: none;
                        display: flex;
                        .social{
                            padding: 0 10px;
                            cursor: pointer;
                        }
                    }
                }
            }

            .footerInferiorDiv{
                text-align: center;
                color: #CCCCCC;
                padding-top: 30px;
            }
        }
    }

</style>