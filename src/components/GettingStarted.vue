<template>
    <div class="get_start">
        <div class="container">
            <h1 class="title">Getting Started Is <br> <strong>Fast & Easy</strong></h1>
            <div class="steps">
                <div class="steps-item">
                    <div class="steps-item-number">01.</div>
                    <div class="steps-item-title">Register</div>
                    <div class="steps-item-text"><p>Complete the simple registration to get your trading credentials.</p></div>
                </div>
                <div class="steps-item margin">
                    <div class="steps-item-number">02.</div>
                    <div class="steps-item-title">Verification</div>
                    <div class="steps-item-text"><p>Big Invest is required to verify your identity, upload your documents quickly and get approved in minutes.</p></div>
                </div>
                <div class="steps-item">
                    <div class="steps-item-number">03.</div>
                    <div class="steps-item-title">Deposit funds</div>
                    <div class="steps-item-text"><p>Big Invest accepts credit cards and bank wires. Just use the secure deposit form and follow the steps.</p></div>
                </div>
                <div class="steps-item">
                    <div class="steps-item-number">04.</div>
                    <div class="steps-item-title">Start Trading</div>
                    <div class="steps-item-text"><p>Once your deposit has been credited, you can begin trading instantly. In no time you will see profits rolling into your account.</p></div>
                </div>
                <div class="dotted-line1">
                    <dot-bg-right/>
                </div>
                <div class="dotted-line2">
                    <dot-bg-left/>
                </div>
                <div class="dotted-line3">
                    <dot-bg-right/>
                </div>
            </div>
            </div>
        </div>
</template>

<script>
    import DotBgLeft from "./icons/dotBgLeft";
    import DotBgRight from "./icons/dotBgRight";
    export default {
        name: "GettingStarted",
        components: {DotBgRight, DotBgLeft}
    }
</script>

<style lang="scss">
.get_start{
    position: relative;

    .container{
        .title{
            margin-top: 140px;
            font-size: 56px;
            @media (max-width: 740px) {
                font-size: 40px;
            }
        }
        .steps{
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            justify-content: space-between;
            position: relative;
            max-width: 1098px;
            margin: 60px auto 0;
            @media (max-width: 1060px) {
                max-width: 688px;

            }
            @media (max-width: 740px) {
                flex-direction: column;
                justify-content: center;
                flex-wrap: nowrap;
                align-items: center;
            }
            .dotted-line2{
                position: absolute;
                right: 44%;
                top: 39%;
                z-index: -1;
                @media (max-width: 1060px) {
                    right: 23%;
                    top: 43%;
                }
                @media (max-width: 740px) {
                    display: none;
                }
            }
            .dotted-line1{
                position: absolute;
                right: 21.5%;
                top: 12%;
                z-index: -1;
                @media (max-width: 1060px) {
                    right: 24%;
                    top: 14%;

                }
                @media (max-width: 740px) {
                    display: none;
                }
            }
            .dotted-line3{
                position: absolute;
                right: 21.5%;
                top: 62%;
                z-index: -1;
                @media (max-width: 1060px) {
                    right: 24%;
                    top: 14%;

                }
                @media (max-width: 740px) {
                    display: none;
                }
            }
            &-item{
                max-width: 483px;
                width: 100%;
                padding: 32px;
                border: 2px solid #6248FF;
                border-radius: 30px;
                box-sizing: border-box;
                /*margin-bottom: 135px;*/
                max-height: 233px;
                background: white;
                @media (max-width: 1060px) {
                    max-width: 329px;
                    max-height: 263px;
                }
                @media (max-width: 740px) {
                    margin-bottom: 24px;
                    max-height: 100%;
                }
                &:nth-child(2n){
                    margin-top: 170px;
                    @media (max-width: 740px) {
                        margin-top: 0;
                    }

                }

                &-number{
                    font-size: 15px;
                    line-height: 18px;
                    color: #6248FF;
                    margin-bottom: 8px;
                }
                &-title{
                    font-weight: 600;
                    font-size: 24px;
                    color: #333333;
                    margin-bottom: 24px;


                }
                &-text{
                    font-size: 18px;
                    line-height: 30px;
                    color: #4F4F4F;
                    font-weight: 300;
                }
            }

        }
    }
}
.margin{
    margin-top: 156px!important;
    @media (max-width: 1060px) {
        margin-top: 190px!important;
    }
    @media (max-width: 740px) {
        margin-top: 0!important;
    }

}
</style>