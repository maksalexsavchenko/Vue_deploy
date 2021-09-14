<template>
    <div :class="open ? 'faq open' : 'faq'" @click="$emit('toggleOpen', index)">
        <div class="question">
            <p class="question-title">{{ faq.question }}</p>
        </div>
        <div class="answer">{{ faq.answer }}</div>
    </div>
</template>

<script>
    export default {
        name: 'FAQ',
        props: ['faq', 'index', 'open']
    }
</script>

<style lang="scss">

    .faq {
        display: block;
        width: 100%;
        max-width: 995px;
        margin: 15px auto;
        padding: 32px 40px;
        border: 2px solid #6248FF;
        border-radius: 20px;
        background-color: #FFF;
        box-sizing:border-box;
        -moz-box-sizing:border-box;
        -webkit-box-sizing:border-box;
        @media (max-width: 1200px){
            max-width: 688px;

        }
        @media (max-width: 600px){
            padding: 24px 16px;

        }
    }
    .faq .question {
        position: relative;
        color: #4F4F4F;
        font-family: "Museo Sans Cyrl";
        font-size: 24px;
        transition: all 0.4s linear;
        margin: 0;
        &-title{
            margin: 0;
        }
        @media (max-width: 600px){
            font-size: 18px;
            padding-right: 30px;
            p{
                margin: 0;
            }


        }

    }
    .faq .question::after {
        content: '';
        position: absolute;
        top: 50%;
        right: 0px;
        transform: translateY(-50%) rotate(0deg);
        width: 18px;
        height: 18px;
        background-image: url('../assets/images/listimg.svg');
        background-position: center;
        background-size: contain;
        background-repeat: no-repeat;
        transition: all 0.3s linear;
    }
    .faq.open .question {
        margin-bottom: 15px;

    }
    .faq.open .question::after {
        transform: translateY(-50%) rotate(45deg);
        opacity: 0.5;
    }
    .faq .answer {
        color: #4F4F4F;
        font-weight: 300;
        font-family: Montserrat;
        font-size: 16px;
        opacity: 0;
        max-height: 0px;
        overflow-y: hidden;
        transition: all 0.4s ease-out;
        line-height: 27px;
    }
    .faq.open .answer {
        opacity: 1;
        max-height: 1000px;
    }
</style>