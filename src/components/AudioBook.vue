
<script>
export default {
    name:"AudioBook",
    
}
</script>

<template>

    <section class="sponsor">

        <div class="sponsorsDiv">
            <div class="sponsorDiv">
                <img src="../assets/img/ebay-logotan-2x.png" alt="ebay">
            </div>
            <div class="sponsorDiv">
                <img src="../assets/img/audible-logotan-2x.png" alt="audible">
            </div>
            <div class="sponsorDiv">
                <img src="../assets/img/bb-logotan@2x.png" alt="barnes&noble">
            </div>
            <div class="sponsorDiv">
                <img src="../assets/img/kindlefire-logotan-2x-600x197.png" alt="Kindle">
            </div>
        </div>

        <div class="newAudioBook">

        </div>

    </section>

    <section class="audioBook">

        <div class="imgDiv">
            <img src="../assets/img/audible-app-2x.png" alt="audible app">
        </div>

        <div class="infoAudioBookDiv">
            <h2>New Audiobook</h2>
            <h4>NO TIME TO READ? NO PROBLEM. LISTEN TO IT</h4>
            <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus.</p>
            
            <div class="d-flex">
                <div class="divImg">
                    <img src="../assets/img/audible-logo.png" alt="audible">
                </div>
                <div class="divImg">
                    <img src="../assets/img/bn-logo-tall.png" alt="barnes&noble">
                </div>
                <div class="divImg">
                    <img src="../assets/img/kindle-logo-tall.png" alt="kindle">
                </div>
            </div>
        </div>

    </section>

</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    .sponsor{
        background-color: #FEF7E9;
        padding: 3%;
        @include centerFlex("orizontal");
        justify-content: center;

        .sponsorsDiv{
            display: flex;
            align-items: center;

            .sponsorDiv{
                width: 25%;
                display: flex;
                align-items: center;

                img{
                    width: 100%;
                    padding: 0 40px;
                    object-fit: contain;
                    max-width: 280px;
                }
            }

        }
    }

    .audioBook{
                width: 100vw;
                background-image: url("../assets/img/banner.jpg");
                background-repeat: no-repeat;
                background-size: cover; 
                background-position: center;
                padding: 4% 5% 0;
                @include centerFlex("both");

                .imgDiv{
                    width: 30%;
                    height: 100%;

                    img{
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
                    }
                }

                .infoAudioBookDiv{
                    width: 40%;
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    align-items: center;

                    h2{
                        font-family: "DM Serif Display",serif;
                        color: white;
                        font-size: 40px;
                        padding: 20px 0;
                    }

                    h4{
                        color: $primary-color;
                        text-align: center;
                        font-size: 18px;
                        padding: 0px 0 20px;
                    }

                    p{
                        color: #999794;
                        font-size: 18px;
                        text-align: center;
                    }

                    div{
                        justify-content: space-around;
                        align-items: center;
                        width: 100%;

                        .divImg{
                            width: 20%;

                            img{
                                width: 100%;
                                object-fit: contain;
                            }
                        }
                    }
                }
            }

</style>