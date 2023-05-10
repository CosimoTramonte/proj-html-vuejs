
<script>
export default {
    name: "Subscribe"
}
</script>

<template>

    <section class="subscribe">

        <div class="subDiv d-flex flex-column align-items-center">
            <h2>Subscribe To My Newsletter</h2>
            <h4>BE NOTIFIED ABOUT BOOK SIGNING TOUR DATES</h4>
            <div class="inputDiv">
                <input type="text">
                <button>Subscribe</button>
            </div>
            <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt.</p>
        </div>

    </section>
  
</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    .subscribe{
        width: 100vw;
        background-image: url("../assets/img/banner-2.jpg");
        background-repeat: no-repeat;
        background-size: cover; 
        background-position: center;
        padding: 9% 5%;
        @include centerFlex("both");
        position: relative;

        &::before{
            content: "";
            position: absolute;
            top: 0; 
            left: 0;
            width: 100%; 
            height: 100%;
            background-color: rgba(0, 0, 0, 0.37);
        }

        .subDiv{
            z-index: 3;
        }

        h2{
            color: white;
            font-size: 40px;
            font-family: "DM Serif Display",serif;
            text-align: center;
        }

        h4{
            color: #F4B429;
            text-align: center;
            font-size: 18px;
            padding: 20px 0 20px;
        }

        .inputDiv{
            text-align: center;
            padding-bottom: 20px;

            input{
                margin-right: 10px;
                width: 50%;
                padding: 6px;
            }

            button{
                padding: 8px 10px;
                background-color: #49A987;
                border: 1px solid #49A987;
                color: white;
                border-radius: 10px;
            }

        }

        p{
            color: #737A82;
            padding: 0 20px;
            font-weight: 400;
            font-family: "DM Sans", Arial, Helvetica, sans-serif;
            font-size: 18px;
            text-align: center;
        }
    }

</style>