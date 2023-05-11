
<script>
export default {
    name:"RecentArticles"
}
</script>

<template>

    <section class="d-flex justify-content-center flex-column align-items-center">

        <div class="TitlesDiv">

            <div class="TitleDiv">
                <h2>Recent Articles</h2>
                <h4>READ THE LATEST ENTRIES</h4>
            </div>
            <button>All Articles</button>

        </div>

        <div class="mainDiv">

            <div class="mainImgDiv">

                <img src="../assets/img/20-Tips-scaled.jpg" alt="img">

                <div class="infoDiv">
                    <h3>20 Creativity Tips</h3>
                    <p>By admin | October 24th, 2019 | Categories: Event, Tips & Tricks</p>
                    <p>Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Donec velit neque, auctor sit amet aliquam vel, ullamcorper sit amet.</p>
                </div>
            </div>

            <div class="secondaryImgDivs">

                <div class="firstSecondaryDiv">
                    <img src="../assets/img/thumb-13-2x-700x441.jpg" alt="img">

                    <div class="infoDiv">
                        <h3>What’s On Your Booklist</h3>
                        <p>By admin | October 24th, 2019</p>
                    </div>
                </div>

                <div class="secondSecondaryDiv">
                    <img src="../assets/img/thumb-08-2x-320x202.jpg" alt="img">

                    <div class="infoDiv">
                        <h3>Istanbul Travel Guide</h3>
                        <p>By admin | October 24th, 2019</p>
                    </div>
                </div>

            </div>

        </div>


    </section>
  
</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    section{
        background-color: #FEF7E9;
    }

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
                font-weight: 500;
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

    .mainDiv{
        @include centerFlex("vertical");
        justify-content: space-between;
        align-items: stretch;
        width: 80%;
        padding: 2% 5% 5%;
        min-height: 300px;

        .mainImgDiv{
            width: 65%;
            background: white;
            padding: 4%;

            &:hover{
                img{
                    filter:brightness(1.5);
                    filter: hue-rotate(90deg);
                    filter: opacity(90%);
                    cursor: pointer;
                }
            }
            
            img{
                cursor: pointer;
                width: 100%;
                object-fit: contain;
                padding-bottom: 4%;
                transition: all 0.4s;
            }

            .infoDiv{

                padding: 1% 3% 0;

                h3{
                    font-size: 28px;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;
                }

                p{
                    color: #737A82;
                    font-weight: 400;
                    font-family: "DM Sans", Arial, Helvetica, sans-serif;
                    font-size: 18px;
                }

                p:first-of-type{
                    font-size: 14px;
                }
            }
        }
        .secondaryImgDivs{
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            width: 30%;
            background: white;
            padding: 3%;

            .firstSecondaryDiv{
                width: 100%;
                height: 45%;
                position: relative;
                overflow-y: hidden;  
                cursor: pointer;          

                &:hover .infoDiv{
                    bottom: -200px 
                }

                img{
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }

                .infoDiv{
                    background-color: white;
                    padding: 30px 25px 20px 25px;
                    position: absolute;
                    margin-left: auto;
                    margin-right: auto;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    transition: all 1s;

                    h3{
                        font-size: 26px;
                        font-family: "DM Sans", Arial, Helvetica, sans-serif;
                    }
                    
                    p{
                        font-size: 14px;
                        font-family: "DM Sans", Arial, Helvetica, sans-serif;
                        color: #737A82;
                    }
                }
            }

            .secondSecondaryDiv{
                width: 100%;
                height: 45%;
                position: relative;
                overflow-y: hidden;            
                cursor: pointer;

                &:hover .infoDiv{
                    bottom: -200px ;
                }

                img{
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }

                .infoDiv{
                    background-color: white;
                    padding: 30px 25px 20px 25px;
                    position: absolute;
                    margin-left: auto;
                    margin-right: auto;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    transition: all 1s;

                    h3{
                        font-size: 26px;
                        font-family: "DM Sans", Arial, Helvetica, sans-serif;
                    }

                    p{
                        font-size: 14px;
                        font-family: "DM Sans", Arial, Helvetica, sans-serif;
                        color: #737A82;
                    }
                }
            }
        }
    }

</style>