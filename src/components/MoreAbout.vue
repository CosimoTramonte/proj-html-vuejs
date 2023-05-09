
<script>
export default {
    name: "MoreAbout",
}
</script>

<template>

    <section>

        <div class="moreAboutDiv">
            <h1>More About Damon Vaughn</h1>
            <p>Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller “The story of my life.”</p>
            <button>Meet The Author</button>
        </div>

    </section>

</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    section{
        @include centerFlex("both");
        margin-top: 50px;

        .moreAboutDiv{
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 80%;
            padding: 5%;

            h1{
                font-family: Kristi,serif;
                color: $primary-color;
                font-size: 90px;
            }

            p{
                font-size: 30px;
                text-align: center;
                padding: 15px 0;
            }

            button{
                width: 180px;
                padding: 8px 10px;
                background-color: #49A987;
                border: 1px solid #49A987;
                color: white;
                border-radius: 10px;

                &:hover{
                    background-color:#357F60;
                    color: white;
                }
            }
        }
    }


</style>