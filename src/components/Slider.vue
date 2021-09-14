<template>
    <div class="slider">
        <div class="container">
            <sliderTab/>
            <sliderMob/>
            <div class="slider_block">
                <div class="title">
                    <h1>People love <br><strong>Big Invest</strong></h1>
                    <div class="arrows">
                        <div class="arrow-prev"
                             v-on:click="prev">
                            <arrowLeft/>
                        </div>
                        <div class="arrow-next"
                             v-on:click="next">
                            <arrowRight/>
                        </div>
                    </div>
                </div>
                <div class="article_block">
                    <articles/>
                    <div class="content">
                        <Slick class="articles" ref="slick" :options="slickOptions" @afterChange="handleAfterChange">
                            <div class="slick-item article" v-if="slides" v-for="item in slides">
                                <div class="author-info">
                                    <div class="avatar">
                                        <img :src="item.image" alt="">
                                    </div>
                                    <div class="author-info-bio">
                                        <h3 class="author">{{item.name}}</h3>
                                        <p class="department">{{item.department}}</p>
                                    </div>
                                </div>

                                <div class="article_text">
                                    <h3>{{item.desc}}</h3>
                                </div>
                            </div>
                        </Slick>
                        <span class="pagination"><strong>{{currentSlide}}</strong> / {{slides.length}}</span>
                    </div>
                </div>

            </div>

<!--            <button type="button" v-on:click="next" class="slick-next">Text</button>-->
<!--            <button type="button"  class="slick-next">Text</button>-->


        </div>
    </div>

</template>

<script>
    import Slick from 'vue-slick'
    import ArrowLeft from "./icons/arrowLeft";
    import ArrowRight from "./icons/arrowRight";
    import Articles from "./icons/articles";
    import SliderTab from "./sliderTab";
    import SliderMob from "./sliderMob";


    export default {
        name: "Slider",
        components: {
            ArrowLeft,
            ArrowRight,
            Articles,
            Slick,
            SliderTab,
            SliderMob
        },
        data() {
            return {
                currentSlide: 1,
                slides: [
                    {
                        name : 'Albert Abello',
                        department: 'Director of Growth',
                        desc: 'This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.',
                        image: require('@/assets/Author.png'),

                    },
                    {
                        name : 'Abello Albert ',
                        department: 'Director of Growth',
                        desc: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s',
                        image: require('@/assets/Author.png'),
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
    .slider{
        .container{
            .slider_block{
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                padding: 140px 0;
                @media (max-width: 1200px) {
                    display: none;
                }
                .title{
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
                .article_block{
                    margin-top: 27px;
                    margin-left: 15px;
                    display: flex;
                    flex-direction: row;
                    .article-icon{
                        @media (min-width: 1200px) {
                            max-height: 40px;
                            margin-top: 100px;
                            margin-right: 20px;
                        }

                    }
                    .articles{
                        max-width: 633px;
                        .article{
                            display: flex!important;
                            flex-direction: column;
                            .author-info{
                                display: flex;
                                flex-direction: row;
                                .avatar{
                                    margin-right: 30px;
                                }
                                &-bio{
                                    .author{
                                        margin: 0;
                                        line-height: 30px;
                                        font-size: 18px;
                                    }
                                    .department{
                                        margin: 0;
                                        font-size: 16px;
                                        line-height: 27px;
                                    }
                                }

                            }

                            &_text{
                                font-size: 24px;
                            }

                        }

                    }
                    .pagination{
                        font-weight: 600;
                        font-size: 15px;
                        color: #4F62F6;
                        strong{
                            color: #6248FF;
                            font-weight: 600;
                            font-size: 15px;
                        }
                    }
                }
            }
        }
    }


</style>