<template>
  <div id="app">
    <Header/>
    <HeroBlock/>
    <GettingStarted/>
    <Slider/>
    <Swiper/>
    <Questions/>
    <FAQ
            v-for="(faq, i) in faqs"
            :faq="faq"
            :index="i"
            :key="i"
            :open="faq.open"
            @toggleOpen="toggleOpen"
    />
    <Contacts/>
    <Footer/>
  </div>
</template>

<script>
import HeroBlock from "./components/HeroBlock";
import Header from "./components/Header";
import GettingStarted from "./components/GettingStarted";
import Questions from "./components/Questions";
import Contacts from "./components/Contacts";
import Footer from "./components/Footer";
import FAQ from "./components/FAQ";
import Slider from "./components/Slider";




export default {
  name: 'App',
  components: {
    Footer,
    HeroBlock,
    Header,
    GettingStarted,
    Questions,
    Contacts,
    FAQ,
    Slider,


  },
  data () {
    return {
      faqs: [
        {
          question: "How do I change my details?",
          answer: "I'm not sure but Lorem ipsum dolor.....",
          open: false
        },
        {
          question: "What platforms will I be able to use?",
          answer: "We provide only the best trading software. The trading terminal MetaTrader4 is the most popular and convenient platform for access to global exchanges. You can work anywhere. All you need is the Internet because the necessary trading tools are already collected in one place and are available in a couple of clicks. Use only the best and develop with us!",
          open: false
        },
        {
          question: "How do I change my details?",
          answer: "I'm not sure but Lorem ipsum dolor.....",
          open: false
        },
        {
          question: "How do I change my details?",
          answer: "I'm not sure but Lorem ipsum dolor.....",
          open: false
        },
        {
          question: "How do I change my details?",
          answer: "I'm not sure but Lorem ipsum dolor.....",
          open: false
        },
        {
          question: "How do I change my details?",
          answer: "I'm not sure but Lorem ipsum dolor.....",
          open: false
        },
        {
          question: "How do I change my details?",
          answer: "I'm not sure but.....",
          open: false
        },
      ]
    }
  },
  methods: {
    toggleOpen: function (index) {
      this.faqs = this.faqs.map((faq, i) => {
        if (index === i) {
          faq.open = !faq.open;
        } else {
          faq.open = false;
        }
        return faq;
      });
    }
  }
}
</script>

<style lang="scss">

  @import "./styles/app.scss";

  @font-face {
    font-family: Montserrat;
    src: local("Montserrat"),
    url(./fonts/Montserrat-Regular.ttf) format("truetype");
  }
  @font-face {
    font-family: "Museo Sans Cyrl";
    src: local("Museo Sans Cyrl"),
    url(./fonts/MuseoSansCyrl-700.ttf) format("truetype");
  }


body{
  margin: 0;
  font-family: Museo Sans Cyrl;
  position: relative;
}
  .container {
    width: 100%;
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
    @media (max-width: 1300px){
      padding: 0 40px;
    }
    @media (max-width: 450px){
      padding: 0 20px;
    }
  }
  h1 {
    font-size: 64px;
    color: #333333;
    margin: 0;
    strong{
      background: #EFEDFF;
    }
  }
  p{
    font-family: Montserrat;
    font-size: 18px;
    color: #333333;
  }

  .btn{
    background: #4F62F6;
    color: white;
    font-size: 16px;
    text-transform: uppercase;
    border-radius: 60px;
    padding: 20px 64px;
    text-decoration: none;
    transition: ease-in-out 0.3s;
    &:hover{
      background: #7181FC;
    }
    &:active{
      background: #354BF4;
    }
  }

  .faq {
    display: block;
    width: 100%;
    max-width: 768px;
    margin: 15px auto;
    padding: 33px 40px;
    border: 2px solid #6248FF;
    border-radius: 20px;

    background-color: #FFF;
  }
  .faq .question {
    position: relative;
    color: #4F4F4F;
    font-family: "Museo Sans Cyrl";
    font-size: 24px;
    transition: all 0.4s linear;
  }
  .faq .question::after {
    content: '';
    position: absolute;
    top: 50%;
    right: 0px;
    transform: translateY(-50%) rotate(0deg);
    width: 18px;
    height: 18px;
    background-image: url('./assets/images/listimg.svg');
    background-position: center;
    background-size: contain;
    background-repeat: no-repeat;
    transition: all 0.3s linear;
  }
  .faq.open .question {
    margin-bottom: 15px;
  }
  .faq.open .question::after {
    transform: translateY(-50%) rotate(45deg);
    opacity: 0.5;
  }
  .faq .answer {
    color: #4F4F4F;
    font-weight: 300;
    font-family: Montserrat;
    font-size: 16px;
    opacity: 0;
    max-height: 0px;
    overflow-y: hidden;
    transition: all 0.4s ease-out;
    line-height: 27px;
  }
  .faq.open .answer {
    opacity: 1;
    max-height: 1000px;
  }

</style>
