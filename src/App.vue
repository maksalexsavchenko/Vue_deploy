<template>
  <div id="app">
    <Header/>
    <HeroBlock/>
    <GettingStarted/>
    <Questions/>

  </div>
</template>

<script>
import HeroBlock from "./components/HeroBlock";
import Header from "./components/Header";
import GettingStarted from "./components/GettingStarted";
import Questions from "./components/Questions";



export default {
  name: 'App',
  components: {
    HeroBlock,
    Header,
    GettingStarted,
    Questions,

  }
}
</script>

<style lang="scss">
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

</style>
