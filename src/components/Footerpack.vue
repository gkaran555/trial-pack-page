<template>
  <section class="test-ackage">
      <div class="test-ackage-left">
        <img src="../../public/img/pa1.png" alt="Lillydoo Windel Design - Little Blowballs">
        <div class="test-ackage_details">
          <h4>10 Lillydoo Windeln</h4>
          <ul>
            <li>0 % Parfüme &amp; Lotionen, 100 % LILLYDOO Schutz</li>
            <li>Extra weich und mit idealer Passform</li>
          </ul>
        </div>
      </div>

      <div class="test-ackage-left">
        <img :src="secondstep.secondstep.phototwo" alt="LILLYDOO 15 Feuchttücher mit 99% Wasser">
        <div class="test-ackage_details">
          <h4>15 Feuchttücher mit 99 % Wasser</h4>
          <ul>
            <li>0 % Parfüme &amp; PEGs, 100 % biologisch abbaubar</li>
            <li>Natürlich rein, extra mild, Alternative zu "Wasser &amp; Watte"</li>
          </ul>
        </div>
      </div>
    </section>   
</template>

<script>
export default {
  name: 'Footerpack',
  props: {
    secondstep: {
        type: Object
    }
  }
 
}
</script>

<style lang="scss" scoped>
@import '../assets/global.scss';

.test-ackage {
  padding: 2rem 1rem 2rem 1rem;
  background: white;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  grid-gap: 7px;
  align-items: center;
  justify-items: center;
  .test-ackage-left {
    display: flex;
    margin-bottom: 20px;
  }
  .test-ackage_details{
    display: flex;
    flex-direction: column;
    h4 {
      text-transform: uppercase;
      font-size: 1.063rem;
      line-height: 1.5;
      margin-bottom: 10px;
    }
    li {
        font-size: .938rem;
        list-style: disc;
        margin-left: 1.1rem;
    }
  }
  img {
    width: 25%;
    height: 30%;
    margin-right: 20px;
  }
}

</style>
