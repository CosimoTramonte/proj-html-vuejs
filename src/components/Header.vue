
<script>
import { NavMenu } from "../data/data.js"

export default {
    name: "Header",
    data(){
        return{
            NavMenu
        }
    }
}
</script>

<template>

  <div class="ct-container">

    <div class="logoDiv">
        <img src="../assets/img/author-logo-round.png" alt="logo author">
    </div>

    <nav>
        <ul>
            <li v-for="(li,index) in NavMenu" :key="index" :class="{'active' : li.isActive}"><a href="#">{{ li.text }}</a></li>
        </ul>
    </nav>

  </div>

</template>


<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    .ct-container{
        height: 90px;
        @include centerFlex("both");
        justify-content: space-between;
        margin: 0 80px;

        .logoDiv{
            height: 100%;

            img{
                height: 160%;
            }
        }

        nav{
            height: 100%;

            ul{
                @include centerFlex("both");
                height: 100%;

                li{
                    height: 100%;
                    list-style: none;
                    @include centerFlex("vertical");
                    padding: 18px;
                    padding-top: 35px;
                    border-top: 5px solid transparent;

                    &.active{
                        border-top: 5px solid $primary-color;

                        a{
                            color: $primary-color;
                        }
                    }

                    a{
                        text-decoration: none;
                        color: $white-text;
                    }
                }
            }
        }
    }
</style>