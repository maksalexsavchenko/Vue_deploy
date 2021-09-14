<template>
    <div class="footer_block">
        <div class="container">
            <div class="menu">
                <div class="logo">
                    <img src="@/assets/images/LOGO.svg" alt="Logo">
                </div>
                <div class="info">
                    <h4>Information and high risk warning:</h4>
                    <p>Trading with foreign exchange (FX), contract for differences (CFDs) and precious metals carries a high level of risk that may not be suitable for all investors. Leverage creates additional risk and loss exposure. Before you decide to trade foreign exchange or contract for differences, carefully consider your investment objectives, experience level, and risk tolerance.</p>
                </div>
                <div class="info">
                    <h4>Legal disclaimer:</h4>
                    <p>Forex trading entails significant risks and is not appropriate for all investors. The possibility of incurring substantial losses should be taken into account. It is therefore important to understand the possible consequences of investing. Traders should weigh their earning potential against the risks involved and act accordingly. Interactive Trade Ltd operating under brand and using domenLink domain within the European Economic Area.</p>
                </div>
                <div class="nav_menu">
                    <ul>
                        <li><a href="">About us</a></li>
                        <li><a href="">Instructions</a></li>
                        <li><a href="">Platforms</a></li>
                        <li><a href="">Contact Us</a></li>
                        <li><a href="">Sign in</a></li>
                        <li><a href="">Sign up for free</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyrights">
                <ul>
                    <li>Copyright 2020, All Right Reserved</li>
                    <li><a href="#">Terms and Conditions</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Risk Warnings</a></li>
                    <li><a href="#">Anti-Money Laundering</a></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        name: "Footer"
    }

</script>

<style lang="scss">
    .footer_block{
        padding: 32px 0 72px;
        @media (max-width: 1200px){
            padding: 0 0 72px 0;
        }
        .container{
            display: flex;
            flex-direction: column;
            .menu{
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                margin-bottom: 46px;
                @media (max-width: 1200px) {
                    flex-direction: column;
                    align-items: center;
                }

                .logo{
                    margin-right: 100px;
                    @media (max-width: 1200px) {
                        order: 1;
                        text-align: center;
                        margin-right: 0;
                        padding: 62px 0 54px 0;
                    }
                }
                .info{
                    max-width: 380px;
                    @media (max-width: 1200px) {
                        order: 3;

                        max-width: 508px;
                    }
                    h4{
                        margin-top: 0;
                        font-size: 18px;
                        @media (max-width: 1200px) {
                            text-align: center;
                        }
                    }
                    p{
                        font-size: 16px;
                        font-weight: 300;
                        line-height: 27px;
                        color: #4F4F4F;


                    }
                }
                .nav_menu{
                    @media (max-width: 1200px) {
                        order: 2;
                        width: 100%;
                        padding-bottom: 40px;
                    }
                    ul{
                        padding: 0;
                        list-style: none;
                        margin: 0;
                        @media (max-width: 1200px) {
                            display: flex;
                            flex-direction: row;
                            width: 100%;
                            justify-content: space-around;
                        }
                        @media (max-width: 600px){
                            flex-direction: column;
                        }
                        li{
                            padding-bottom: 24px;
                            &:last-child{
                                padding-bottom: 0;
                                @media (max-width: 600px){
                                    padding-bottom: 0;
                                }
                            }
                            @media (max-width: 1200px){
                                padding: 0;
                            }
                            @media (max-width: 600px){
                                padding-bottom: 32px;
                            }

                            a{
                                font-family: "Museo Sans Cyrl";
                                text-decoration: none;
                                font-size: 15px;
                                color: #333333;
                                transition: 0.3s;
                                font-weight: 600;

                                &:hover{
                                    color: #4F62F6;
                                }
                            }
                        }
                    }
                }
            }
            .copyrights{
                width: 100%;
                font-family: 'Montserrat';
                font-weight: 300;
                font-size: 16px;
                color: #828282;
                ul{
                    list-style: none;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    padding-left: 0;
                    @media (max-width: 1200px){
                        flex-direction: column;
                        text-align: center;
                        margin: 0;
                    }
                    li{
                        @media (max-width: 1200px){
                            padding-bottom: 16px;
                            &:last-child{
                                padding-bottom: 0;
                            }
                        }
                        a{
                            text-decoration: none;
                            font-family: 'Montserrat';
                            font-weight: 300;
                            font-size: 16px;
                            color: #828282;
                            transition: 0.3s;
                            &:hover{
                                color: #4F62F6;
                            }
                        }
                    };
                    li:first-child{
                        padding-right: 66px;
                        @media (max-width: 1200px){
                            padding-right: 0;
                        }
                    }
                }
            }
        }
    }
</style>