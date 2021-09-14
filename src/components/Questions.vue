<template>

    <div class="questions_block">
        <div class="container">
            <h1>Frequently asked <br>
                <strong>questions</strong></h1>
        </div>
    </div>
</template>

<script>

    export default {
        name: "Questions",
        props: {
            data: String,
            msg: String
        },
        methods: {

        }
    }
</script>

<style lang="scss">
    .questions_block{
        padding-bottom: 68px;
        @media (max-width: 600px) {
            padding-bottom: 30px;
        }
    }
</style>