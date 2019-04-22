<template>
    <header>
        <div class="header-inner">
            <h1 class="header-title">Entdecke unsere <br> Hautfreundlichkeit</h1>
            <button>JETZT DEINE GRÖSSE WÄHLEN</button>
        </div>
        <img src="../../public/img/tex.gif" alt="Oeko-Tex Certificate" class="header-img">
    </header> 
</template>

<script>
export default {
  name: 'Headerpack'
}
</script>

<style lang="scss" scoped>
@import '../assets/global.scss';

header {
  background-image: url("../../public/img/LLYD_web_trialpack_website_sample_task_1903-3.gif");
  background-repeat:no-repeat;
  background-position: center;
  background-size: 100% 100%;
  height: 37vw;
  min-height: 320px;
  display: flex;
  align-items: center;
  position: relative;
  .header-inner {
     margin-left: 12%; 
     text-align: center;
      @media screen and (max-width: $bp-large) and (min-width: $bp-medium) {margin-left: 7%;}
  }
  .header-title {
    font-family: Museo-300,Helvetica,Roboto,Arial,sans-serif;
    font-size: 2.625rem;
    line-height: 1.1;
    margin-bottom: 10px;
    font-style: normal;
    font-weight: 400;
    @media only screen and (max-width: $bp-medium) {
      br {display: none;}}
  }
  .header-img {
    position: absolute;
    top: 14%;
    right: 5%;
    width: 12%;
  }
  @media only screen and (max-width: $bp-medium) {
    background-image: url("../../public/img/LLYD_web_trialpack_website_sample_task_1903-7.gif");
    flex-direction: column;
    justify-content: space-between;
    height: 80vh;
     .header-inner {    
        margin-top: 12%; 
        margin-left: 0%; 
        width: 80%;
      }
      .header-title {
        font-size: 2.188rem;
        @media only screen and (max-width: $bp-smallest) {font-size: 1.5rem;}
      }
      .header-img {
        top: 56%;
        right: 12%;
        width: 15%;
        @media only screen and (max-width: $bp-smallest) {width: 25%; top: 53%;}
      }     
  }
}
</style>


    