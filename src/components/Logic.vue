<template>
  <div class="trialpack-slider">

    <div class="trialpack-slider-img">
      <img :src="secondstep.stepphoto">
    </div>

    <div class="trialpack-slider-info">
        <h2>Unser gratis Testpaket</h2>
        <p>WäHLE DEINE GROßE</p>

        <ul class="trialpack-slider-info-box" >
          <li v-for="step in steps" :key="step.name" v-on:click="greet(step)" :class="{'active' : activecat == step.name}">
            <p>{{step.name}}</p>
            <span>{{step.kg}}</span>
          </li>
        </ul>
        
        <p>Teste jetzt unsere Windeln und Feuchttücher - In Größe 1 - 3 enthält unser Testpaket unsere Feuchttücher mit 99 % Wasser, ab Gr. 4 erhältst Du unsere Sensitiven Feuchttücher. Wir zahlen die Produkte, Du nur den Versand.</p>
        <ul class="trialpack-slider-info-list">
          <li class="primary-color">Automatischer Übergang ins jederzeit kündbare Windel-Abo für 49,50&nbsp;€ pro Lieferung.</li>
          <li>Preise inkl. MwSt., ggf. zzgl. <a href="/de/zahlung-und-versand" target="_blank">Versandkosten</a></li>
        </ul>
        <button>JETZT DEINE GRÖSSE WÄHLEN</button>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Logic',
  data() {
    return {
      steps: [
        { name: '1', kg: '(2-3 KG)', stepphoto: '/img/shot1.gif', phototwo: '/img/pa2.png', isActive : false},
        { name: '2', kg: '(3-4 KG)', stepphoto: '/img/shot2.gif', phototwo: '/img/pa2.png' , isActive : false},
        { name: '3', kg: '(4-37 KG)', stepphoto: '/img/shot3.gif', phototwo: '/img/pa2.png', isActive : false},
        { name: '4', kg: '(7-10 KG)', stepphoto: '/img/shot4.gif', phototwo: '/img/pa3.png', isActive : false},
        { name: '5', kg: '(10-12 KG)', stepphoto: '/img/shot5.gif', phototwo: '/img/pa3.png', isActive : false}
      ],
      secondstep: {name: '1', kg: '(2-3 KG)', stepphoto: '/img/shot1.gif', phototwo: '/img/dd1.png'},
      activecat: "1"
    }
  },
  methods: {
    greet: function (step) {
      this.secondstep = step;
      this.$emit('childToParent', this.secondstep)
      this.activecat = step.name
    }
  }
}
</script>


<style scoped lang="scss">
@import '../assets/global.scss';

.trialpack-slider {
  padding: 3rem 1rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  .trialpack-slider-img {
    @media screen and (max-width: $bp-large) and (min-width: $bp-medium) {width: 45%;}
    text-align: center;
    margin-bottom: 59px;
    img {
      width: 100%;
    }
  }
  .trialpack-slider-info {
    width: 40%;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    @media only screen and (max-width: $bp-medium) {width: 100%;}
    h2 {
      font-size: 1.688rem;
      line-height: 1.2;
      margin-bottom: 10px;
      font-weight: 400;
    }
    p {
      font-size: .938rem;
      margin-bottom: 10px;
    }
    .trialpack-slider-info-box {
        display: flex; 
        @media only screen and (max-width: 332px) {flex-wrap: wrap;}
        justify-content: space-between;
        list-style: none;  
        margin-bottom: 30px;
        li {
          border: 1px solid #7c7c7c;
          text-align: center;
          flex-grow: 1;
          padding: 5px 5px 2px 5px;
          color: #7c7c7c;
          margin-right: 10px;
          margin-bottom: 10px;
          
          &:hover{
            background-color: #00afab;
            border-color: #00afab;
            color: #fff;
            cursor: pointer;
          }
          p {
            font-size: 1.2rem;
            margin: 0px;
          }
          span {
             line-height: 1;
             font-size: .8rem;
             margin: 0px;
          }
       
        }
        .active {
            background-color: #00afab;
            border-color: #00afab;
            color: #fff;
        }
    }
    .trialpack-slider-info-list {
      list-style: disc;
      margin-left: 1.1rem;
      margin-bottom: 2rem;
      .primary-color {
        color: #00afab;
      }
      a {
        color: #00afab;
        text-decoration: none;
      }
    }
  }
}

</style>
