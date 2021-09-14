<template>
    <div class="header">
        <div class="container">
            <div class="navigation">
                <div class="nav_left">
                    <div class="logo">
                        <img src="@/assets/images/LOGO.svg" alt="Logo">
                    </div>
                    <div class="nav_menu">
                        <ul class="menu">
                            <li class="menu-item"><a href="">How it works</a></li>
                            <li class="menu-item"><a href="">About</a></li>
                            <li class="menu-item"><a href="">Instructions</a></li>
                            <li class="menu-item"><a href="">Accounts</a></li>
                            <li class="menu-item"><a href="">Platforms</a></li>
                            <li class="menu-item"><a href="">Contact</a></li>
                        </ul>
                    </div>
                </div>
                <div class="nav-right">
                    <div class="lang">EN <arrowDown/></div>
                    <a href="/" class="btn-sign_in">
                        Sign in for free
                    </a>
                    <div class="burger_menu">
                        <burger/>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script>

    import ArrowDown from './icons/arrowDown'
    import Burger from './icons/burger'

    export default {
        name: "Header",
        components: {
            ArrowDown,
            Burger
        },
    }
</script>

<style lang="scss">
    .header{
        padding: 20px 0;
        position: fixed;
        width: 100%;
        background: white;
        z-index: 99;
        .container{
            @media (max-width: 450px){
                padding: 0 40px;
            }
            .navigation{
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                @media (max-width: 1200px) {
                    justify-content: end;
                }
                @media (max-width: 450px){
                    justify-content: space-between;
                }
                .nav_left{
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    @media (max-width: 1200px) {
                        display: none;
                    }
                    @media (max-width: 450px){
                        display: flex;

                    }
                    .nav_menu{
                        @media (max-width: 450px){
                            display: none;
                        }
                        ul{
                            list-style: none;
                            display: flex;
                            flex-direction: row;
                            justify-content: space-between;
                            width: 100%;
                            li:not(:first-child){
                                padding-left: 32px;
                            }
                            .menu-item{
                                a{
                                    text-decoration: none;
                                    color: #333333;
                                    transition: ease-in-out 0.3s;
                                    &:hover{
                                        color: #4F62F6;
                                    }
                                }
                            }
                        }
                    }
                }
                .nav-right{
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    align-items: center;
                    .lang{
                        border: 1px solid #333333;
                        padding: 10px 16px;
                        border-radius: 60px;
                        display: flex;
                        flex-direction: row;
                        align-items: center;
                        justify-content: space-between;
                        margin-right: 24px;
                        @media (max-width: 1200px) {
                            display: none;
                        }
                    }
                    .btn-sign_in{
                        background: #4F62F6;
                        color: white;
                        font-size: 14px;
                        text-transform: uppercase;
                        border-radius: 60px;
                        padding: 13px 24px;
                        text-decoration: none;
                        transition: ease-in-out 0.3s;
                        @media (max-width: 450px){
                            display: none;
                        }
                        &:hover{
                            background: #7181FC;
                        }
                        &:active{
                            background: #354BF4;
                        }
                    }
                }
            }
        }
    }
</style>