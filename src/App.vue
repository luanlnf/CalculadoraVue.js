<template>
  <div id="app">
    <Intro @setCalculator="setCalculator" />
    <div v-if="calculatorType === 'normal'">
      <CalculatorNormal />
    </div>
    <div v-if="calculatorType === 'scientific'">
      <CalculatorScientific />
    </div>
  </div>
</template>

<script>
import Intro from './components/Intro.vue';
import CalculatorNormal from './components/CalculatorNormal.vue';
import CalculatorScientific from './components/CalculatorScientific.vue';

export default {
  name: 'App',
  components: {
    Intro,
    CalculatorNormal,
    CalculatorScientific,
  },
  data() {
    return {
      calculatorType: null,
    };
  },
  methods: {
    setCalculator(type) {
      this.calculatorType = type;
    },
  },
};
</script>

<style scoped>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  margin: 20px;
}
</style>

