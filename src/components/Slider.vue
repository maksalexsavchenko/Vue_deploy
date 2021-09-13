<template>
    <div class="slider">
        <div class="container">
            <div class="slider_block">
                <div class="title">
                    <h1>People love <br><strong>Big Invest</strong></h1>
                    <div class="arrows">
                        <div class="arrow-prev"
                             v-on:click="prev">
                            <
                        </div>
                        <div class="arrow-next"
                             v-on:click="next">
                            >
                        </div>
                    </div>
                </div>
                <div class="article_block">
                    <Slick class="articles" ref="slick" :options="slickOptions" @afterChange="handleAfterChange">
                        <div class="slick-item article" v-if="slides" v-for="item in slides">
                            <h3 class="span">{{item.name}}</h3>
                            <img :src="item.image" alt="">
                            <p class="span">{{item.department}}</p>
                            <h2 class="span">{{item.desc}}</h2>
                            <span class="span"></span>


                        </div>
                    </Slick>
                    <span>{{currentSlide}} / {{slides.length}}</span>
                </div>

            </div>

<!--            <button type="button" v-on:click="next" class="slick-next">Text</button>-->
<!--            <button type="button"  class="slick-next">Text</button>-->


        </div>
    </div>
</template>

<script>
    import Slick from 'vue-slick'

    export default {
        name: "Slider",
        components: { Slick },
        data() {
            return {
                currentSlide: 1,
                slides: [
                    {
                        name : 'Albert Abello',
                        department: 'Director of Growth',
                        desc: 'This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.',
                        image: '/img/Author.d129eca7.png',

                    },
                    {
                        name : 'Abello Albert ',
                        department: 'Director of Growth',
                        desc: 'This magical product actually works! It has radically changed the way we build our audiences. Increasing new customer sales by 6x in our most mature market.',
                        image: '../assets/images/Author.png',
                    }
                ],
                slickOptions: {
                    infinite: true,
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
                .title{

                }
                .articles{
                    max-width: 633px;
                    .article{
                        display: flex!important;
                        flex-direction: column;
                    }
                }
            }
        }
    }


</style>