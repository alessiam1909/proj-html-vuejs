<script>
export default {
    props: {
        navList: Array
    }
}
</script>

<template lang="">
    <div class="first header">
        <div class="row">
            <div>We have a 95% Successful Pass Rate!</div>
            <div>Give us a call to book your tuition! 1-800-555-555</div>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/variables.scss' as *;
    @use '../styles/partials/mixins.scss' as *;

    .first-header{
        background-color: $black;

        .row{
            @include width80;
        }
    }
</style>