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
        .container{
            display: flex;
            flex-direction: column;
            .menu{
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                .logo{

                }
                .info{

                }
                .nav_menu{
                    ul{
                        padding: 0;
                        list-style: none;
                        li{
                            padding-bottom: 24px;
                            &:last-child{
                                padding-bottom: 0;
                            }
                            a{
                                font-family: "Museo Sans Cyrl";
                                text-decoration: none;
                                font-size: 15px;
                                color: #333333;
                                transition: 0.3s;

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
                    li{
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
                    }
                }
            }
        }
    }
</style>