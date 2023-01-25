<script>
export default {
    
}
</script>

<template lang="">
    <div class="container2">
        <div class="row">
            <div>
                <h1>Start Learning to Drive Today</h1>
                <h3>Give us a call to schedule your first driving lesson</h3>
            </div>
            <div class="number"><i class="fa-solid fa-phone"></i> 1-800-555-555</div>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .container2{
        background-image: url('../assets/images/horizontal-cta-background.jpg');
        background-size: cover;
        height: 250px;
        position: relative;

        .row{
            @include width70;
            @include flex-between;
            color: $white;
            height: 100%;


            h1{
                font-size: 35px;
                margin: 10px 0;
            }

            .number{
                font-size: 30px;
                margin-right: 150px;

                i{
                    margin-right: 30px;
                }
            }
        }
    }
</style>