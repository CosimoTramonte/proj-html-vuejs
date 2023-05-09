
<script>
export default {
    name: "Jumbotron",
}
</script>

<template>

    <div class="container">
        <div class="row">
            <div class="col">
                <h1>Damon Vanghn</h1>
            </div>
            <div class="col"></div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
    @use "../scss/partials/utilities" as *;
    @use "../scss/partials/mixin" as *;

    .container{
        width: 100%;
        height: 100%;

        .row{
            width: 100%;
            height: 100%;

            .col{
                height: 100%;
            }
        }
    }
</style>