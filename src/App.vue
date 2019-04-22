<template>
  <div class="container">
  
    <Headerpack/>

    <main>
      <Logic @childToParent="secondstep = $event"/>

      <div class="interd">
        <h2>Wie es funktioniert</h2>
      </div>

      <section id="trail-step">
          <div class="feature">
            <img src="../public/img/icon1.gif" alt="">
            <h4>Dein Testpaket</h4>
            <p>Wir schenken Dir die Produkte,<br>Du übernimmst nur das Porto.</p>
          </div>

          <div class="feature">
            <img src="../public/img/icon2.gif" alt="">
            <h4>Deine Flexibilität</h4>
            <p>Erste Monatsbox nach 14 Tagen für 49,50&nbsp;€ erhalten. Oder noch vor der ersten Lieferung kündigen.</p>
            <p><a href="/de/windel-abo" target="_blank">Erfahre hier mehr über das <br>LILLYDOO Windel-Abo.</a></p>
          </div>

          <div class="feature">
            <img src="../public/img/icon3.gif" alt="">
            <h4>Deine Monatsbox</h4>
            <p>Jederzeit Designs oder Lieferintervalle anpassen oder die Windelgröße ändern.</p>
          </div>
     </section>

    <div class="interd erpa">
        <h2>Dein Testpaket enthält</h2>
    </div>

    <Footerpack :secondstep="{secondstep}"/>

    </main>

  </div>
</template>

<script>
import Logic from './components/Logic.vue'
import Headerpack from './components/Headerpack.vue'
import Footerpack from './components/Footerpack.vue'

export default {
  name: 'app',
  components: {
    Logic,
    Headerpack,
    Footerpack
  },
  data() {
    return {
      secondstep: {name: 'Goran', stepphoto: '/img/shot1.gif', phototwo: '/img/pa2.png'}
    }
  }
  
}
</script>

<style lang="scss">
@import './assets/global.scss';

#trail-step {
  padding: 0 1rem 2rem 1rem;
  background: #f8f8f8;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 7px;
  .feature {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    img {
      width: 17%;
      margin-bottom: 15px;
    }
    h4 {
      text-transform: uppercase;
      letter-spacing: 0;
      font-size: 1.063rem;
      line-height: 1.5;
      margin-bottom: 10px;
    }
    p {
      font-size: .938rem;
      margin-bottom: 20px;
    }
    a {
      color: #00afab;
      font-size: .938rem;
      text-decoration: none;
    }
  }
}


.interd {
  padding: 3rem 0 2rem 0;
  text-align: center;
  background: #f8f8f8;
  h2 {
    font-size: 1.688rem;
    margin-bottom: 2rem;
    font-style: normal;
    font-weight: 400;
  }    
}
.erpa {
  background: #fff;
}

</style>
