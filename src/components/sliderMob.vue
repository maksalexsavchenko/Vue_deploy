<template>
    <div class="slider_block_mob">
        <div class="title">
            <h1>People love <br><strong>Big Invest</strong></h1>
        </div>
        <div class="slider-content">
            <div class="article_block_mob">
                <div class="content">
                    <Slick class="articles" ref="slick" :options="slickOptions" @afterChange="handleAfterChange">
                        <div class="slick-item article" v-if="slides" v-for="item in slides">
                            <img :src="item.image" alt="">
                            <h3 class="author">{{item.name}}</h3>
                            <p class="department">{{item.department}}</p>
                            <articles/>
                            <div class="article_text">
                                <h3>{{item.desc}}</h3>
                            </div>
                        </div>
                    </Slick>
                    <div class="controls">
                        <div class="arrows">
                            <div class="arrow-prev"
                                 v-on:click="prev">
                                <arrowLeft/>
                            </div>
                        </div>
                        <span class="pagination"><strong>{{currentSlide}}</strong> / {{slides.length}}</span>
                        <div class="arrows">
                            <div class="arrow-next"
                                 v-on:click="next">
                                <arrowRight/>
                            </div>
                        </div>
                    </div>
                </div>
            </div>


        </div>

    </div>

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
                    fade: true,
                    autoplay: true,
                    autoplaySpeed: 4000,
                    infinite: true
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
    .slider_block_mob{
        display: none;
        flex-direction: column;
        justify-content: space-between;
        padding: 140px 0;
        @media (max-width: 800px) {
            display: flex;
        }

        .slider-content{
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            margin-top: 48px;
            .arrows{
                display: flex;
                flex-direction: row;
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
        .article_block_mob{
            display: flex;
            flex-direction: row;
            width: 100%;
            box-sizing: border-box;
            .content{
                text-align: center;
                width: 100%;
                .articles{
                    max-width: 100%;
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
                .controls{
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    align-items: center;
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