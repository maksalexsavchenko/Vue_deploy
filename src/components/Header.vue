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
                    <div class="lang">EN ></div>
                    <a href="/" class="btn-sign_in">
                        Sign in for free
                    </a>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style lang="scss">
    .header{
        padding: 20px;
        position: fixed;
        width: 100%;
        background: white;
        z-index: 99;
        .container{
            .navigation{
                display: flex;
                flex-direction: row;

                justify-content: space-between;
                .nav_left{
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    .nav_menu{
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
                }
            }
        }
    }
</style>