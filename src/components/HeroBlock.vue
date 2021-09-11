<template>
    <div class="hero_block">
        <div class="container">
            <div class="text_block">
                <h1 class="title">Trade everywhere.
                    Invest here!
                </h1>
                <p class="text">We provide only the best trading software.
                    The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere.
                </p>
                    <a href="" class="btn">Start trading</a>
            </div>
            <div class="img">
                <img src="@/assets/images/heroimg.svg" alt="">
            </div>

        </div>

    </div>
</template>

<script>

    export default {
        name: "HeroBlock"
    }
</script>

<style lang="scss">

    .hero_block{
        background: #EFEDFF;
        @media (min-width: 992px){
            padding: 100px 0;
        }
        @media (min-width: 992px){
            padding: 40px 0;
        }
        .container{
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            box-sizing: border-box;
            @media (max-width: 992px){
                flex-direction: column;
                align-items: center;
            }
        }
        .text_block{
            margin: 0 auto;
            padding: 40px 0 0 0;
            @media (max-width: 992px){
                display: flex;
                flex-direction: column;
                align-items: center;
            }
        }
        .title{
            @media (max-width: 992px){
                text-align: center;
            }
            @media (max-width: 450px){
                font-size: 40px;
                text-align: left;
            }
        }
        .text{
            font-size: 18px;
            line-height: 30px;
            font-weight: 200;
            max-width: 483px;
            margin-bottom: 68px;
            color: #4F4F4F;
            margin-top: 32px;
            @media (max-width: 992px){
                text-align: center;
                margin-bottom: 48px;
            }
            @media (max-width: 450px){
                text-align: left;
                margin: 20px 0 32px 0;
            }

        }
        .img{
            width: auto;
            @media (max-width: 992px){
                margin: 32px 0;
                img{
                    width: 100%;
                    position: relative;
                }
            }
        }
    }

</style>