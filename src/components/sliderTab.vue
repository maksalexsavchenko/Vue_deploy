<template>
            <div class="slider_block_tab">
                <div class="title">
                    <h1>People love <br><strong>Big Invest</strong></h1>

                </div>
                <div class="slider-content">
                    <div class="arrows">
                        <div class="arrow-prev"
                             v-on:click="prev">
                            <arrowLeft/>
                        </div>
                    </div>

                    <div class="article_block_tab">
                        <div class="content">
                            <Slick class="articles" ref="slick" :options="slickOptions" @afterChange="handleAfterChange">
                                <div class="slick-item article" v-if="slides" v-for="item in slides">
                                    <h3 class="author">{{item.name}}</h3>
                                    <img :src="item.image" alt="">
                                    <p class="department">{{item.department}}</p>
                                    <articles/>
                                    <div class="article_text">
                                        <h3>{{item.desc}}</h3>
                                    </div>
                                </div>
                            </Slick>
                            <span class="pagination"><strong>{{currentSlide}}</strong> / {{slides.length}}</span>
                        </div>
                    </div>
                    <div class="arrows">
                        <div class="arrow-next"
                             v-on:click="next">
                            <arrowRight/>
                        </div>
                    </div>

                </div>

            </div>
<!--arrows-->
<!--    <div class="arrows">-->


<!--    </div>-->
<!--arrows-->

<!--    content-->

<!--    content-->

</template>

<script>
    import Slick from 'vue-slick'
    import ArrowLeft from "./icons/arrowLeft";
    import ArrowRight from "./icons/arrowRight";
    import Articles from "./icons/articles";



    export default {
        name: "Slider",
        components: {
            ArrowLeft,
            ArrowRight,
            Articles,
            Slick,
        },
        data() {
            return {
                currentSlide: 1,
                slides: [
                    {
                        name : 'Albert Abello',
                        department: 'Director of Growth',
                        desc: 'This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.',
                        image: './src/assets/images/heroimg.svg',

                    },
                    {
                        name : 'Abello Albert ',
                        department: 'Director of Growth',
                        desc: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s',
                        image: '',
                    }
                ],
                slickOptions: {
                    slidesToShow: 1,
                    arrows: false,
                },
            };
        },
        methods: {
            handleAfterChange(event, slick, currentSlide) {
                this.currentSlide = currentSlide+1;
            },
            next() {
                this.$refs.slick.next();
            },

            prev() {
                this.$refs.slick.prev();
            },
        },
    }

</script>

<style lang="scss">
            .slider_block_tab{
                display: none;
                flex-direction: column;
                justify-content: space-between;
                padding: 140px 0;
                @media (max-width: 1200px) {
                    display: flex;
                }
                @media (max-width: 800px) {
                    display: none;
                }

                .slider-content{
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    align-items: center;
                    .arrows{
                        display: flex;
                        flex-direction: row;
                        margin-top: 46px;
                        .arrow-next{
                            border-radius: 90px;
                            border: 1px solid #354BF4;
                            cursor: pointer;
                            width: 48px;
                            height: 48px;
                            align-items: center;
                            display: flex;
                            justify-content: center;
                        }
                        .arrow-prev{
                            border-radius: 90px;
                            border: 1px solid #354BF4;
                            cursor: pointer;
                            width: 48px;
                            height: 48px;
                            align-items: center;
                            display: flex;
                            justify-content: center;
                            margin-right: 16px;
                        }
                    }
                }

                .title{

                }
                .article_block_tab{
                    display: flex;
                    flex-direction: row;
                    .content{
                        text-align: center;

                    }
                    .articles{
                        max-width: 633px;
                        .article{
                            display: flex!important;
                            flex-direction: column;
                            align-items: center;
                            .author{
                                margin: 0;
                                line-height: 30px;
                                font-size: 18px;
                            }
                            .department{
                                margin: 0 0 16px;
                                font-size: 16px;
                                line-height: 27px;

                            }
                            &_text{
                                font-size: 24px;

                                h3 {
                                    margin: 16px 0 32px 0;
                                }
                            }
                        }

                    }
                    .pagination{
                        font-weight: 600;
                        font-size: 15px;
                        color: #4F62F6;
                        text-align: center;
                        strong{
                            color: #6248FF;
                            font-weight: 600;
                            font-size: 15px;
                        }
                    }
                }
            }


</style>