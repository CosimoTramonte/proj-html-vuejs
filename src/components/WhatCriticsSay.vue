
<script>
export default {
    name:"WhatCriticsSay"
}
</script>

<template>

    <section class="d-flex justify-content-center flex-column align-items-center">

        <div class="TitlesDiv">

            <div class="TitleDiv">
                <h2>What The Critics Say</h2>
                <h4>TESTIMONIALS FROM AROUND THE WORLD</h4>
            </div>
            <button>Read All Tesimonials</button>

        </div>

        <div class="TestimonialsDiv">
            
            <div class="mainTestimonial">
                <div class="cardWrapper">

                    <h2>Best Author Of His Generation</h2>
                    <hr>
                    <h6>This book will change your perspective on life</h6>
                    <p>Donec fringilla nunc eu turpis dignissim , at euismod sapien tincidunt . Maecenas eleifend congue cursus . In vitae enim quis sem pharetra.Curabitur arcu erat , accumsan id imperdiet et , porttitor at sem . </p>
                    <p>Donec rutrum congue leo eget malesuada . Vivamus suscipit tortor eget felis porttitor volutpat . Nulla quis lorem ut liber . Proin eget tortor risus . Praesent sapien massa , convallis a pellentesque nec , egestas non nisi . Donec rutrum congue leo eget malesuada .</p>
                    <img src="../assets/img/nytimes-logo-white-xsmall.png" alt="nyTimes">
                    <h6>Justine Kilpatrick, <span>The New York Times</span></h6>

                </div>
            </div>

            <div class="otherTestimonials">

                <div class="secondaryTestimonial">
                    <h3>A True Masterpiece, Bravo!</h3>
                    <p>Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Vivamus suscipit tortor eget felis porttitor volutpat. Nulla quis lorem ut libero malesuada feug at.</p>
                </div>
                <div class="secondaryTestimonialName">
                    <img src="../assets/img/theguardian-xsmall.png" alt="guardian">
                    <h6>Gerald Hendley <span>, The Guardian</span></h6>
                </div>

                <div class="thirdTestimonial">
                    <h3>A Unique View On The World</h3>
                    <p>Donec sollicitudin molestie malesuada. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui. Nulla quis lorem ut libero malesuada feugiat. Vestibulum ac diam sit amet.</p>
                </div>
                <div class="thirdTestimonialName">
                    <img src="../assets/img/globe-xsmall.png" alt="globe">
                    <h6>Mary Maxey <span>, The Globe And Mail</span></h6>
                </div>

            </div>

        </div>

    </section>
  
</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    .TitlesDiv{
        @include centerFlex("vertical");
        justify-content: space-between;
        width: 80%;
        padding: 3% 5% 1%;

        .TitleDiv{

            h2{
                font-family: "DM Serif Display",serif;
                font-size: 40px;
                padding-bottom: 10px;
            }

            h4{
                font-size: 18px;
                color: #49A987;
            }

        }
        
        button{
            padding: 13px 18px;
            background-color: $primary-color;
            border: 1px solid $primary-color;
            color: white;
            border-radius: 10px;
    
            &:hover{
                background-color:#db9601;
                color: white;
            }
        }
    }

    .TestimonialsDiv{
        width: 80%;
        padding: 1% 5% 1%;
        display: flex;
        justify-content: space-between;

        .mainTestimonial{
            background-image: url("../assets/img/testimonial2-2x.jpg");
            background-repeat: no-repeat;
            background-size: cover; 
            background-position: center;
            width: 58%;
            color: $white-text;
            border-end-end-radius: 100px;
            max-height: 780px;
            
            .cardWrapper{
                width: 100%;
                height: 100%;
                background-color: rgba(0, 0, 0, 0.411);
                padding: 15% 16%;
                border-end-end-radius: 100px;
                max-height: 780px;
          
                h2{
                    font-family: "DM Serif Display",serif;
                    font-size: 40px;
                    padding-bottom: 5%;
                }

                h6:first-of-type{
                    font-size: 20px;
                    line-height: 30px;
                    padding: 1% 0;
                }

                p{
                    line-height: 28px;
                    padding: 1% 0;
                }

                h6:last-of-type{
                    display: inline-block;
                    padding-left: 10px;

                    span{
                        color: #49A987;
                    }
                }
            }
        }

        .otherTestimonials{
            width: 40%;
            height: 100%;
            @include centerFlex("orizontal");
            flex-direction: column;

            .secondaryTestimonial{
                width: 90%;
                margin: 0 auto;
                text-align: center;
                background-color: #FEF7E9;
                padding: 8%;

                h3{
                    font-size: 25px;
                    font-family: "DM Serif Display",serif;
                }

                p{
                    color: #737A82;
                    line-height: 30px;
                    padding: 0 20px;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;
                    font-size: 18px;
                }
            }

            .secondaryTestimonialName{
                width: 90%;
                margin: 0 auto;
                padding: 20px 0;

                h6{
                    display: inline-block;
                    margin-left: 20px;
                    padding-bottom: 10%;
                    color: #737A82;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;

                    span{
                        color: black;

                        &:hover{
                            color: $primary-color;
                            cursor: pointer;
                        }
                    }
                }
            }

            .thirdTestimonial{
                width: 90%;
                margin: 0 auto;
                text-align: center;
                background-color: #FEF7E9;
                padding: 8%;

                h3{
                    font-size: 25px;
                    font-family: "DM Serif Display",serif;
                }

                p{
                    color: #737A82;
                    line-height: 30px;
                    padding: 0 2080;
                    font-weight: 400;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;
                    font-size: 18px;
                }
            }

            .thirdTestimonialName{
                width: 90%;
                margin: 0 auto;
                padding: 20px 0;

                h6{
                    display: inline-block;
                    margin-left: 20px;
                    padding-bottom: 10%;
                    color: #737A82;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;

                    span{
                        color: black;

                        &:hover{
                            color: $primary-color;
                            cursor: pointer;
                        }
                    }
                }
            }

        }
    }

    

</style>