<script setup>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      calculo: 'soma',
      resultado: 0,
      };
    },
  methods: {
    calcular() {
      const num1 = parseFloat(this.numero1);
      const num2 = parseFloat(this.numero2);

      switch (this.calculo) {
        case 'soma':
          this.resultado = num1 + num2;
          break;
        case 'subtracao':
          this.resultado = num1 - num2;
          break;
        case 'multiplicacao':
          this.resultado = num1 * num2;
          break;
        case 'divisao':
          this.resultado = num1 / num2;
          break;
          default:
            this.resultado = 0;
      }
    }
  }
</script>

<template>
  <div class="container">
    <header class="p-5 mb-4 mt-4">
      <h1>Calculadora Arítimetica</h1>
      <p>Você poderá fazer várias contas utilizando essa calculadora</p>
    </header>
    <form class="text-center">
      <div class="row">
        <div class="col-md-1">
          <input
            v-model="numero1"
            type="number"
            class="input-number form-control"
          />
        </div>
        <div class="col-md-1">
          <select v-model="calculo" class="form-control text-center">
            <option value="soma">+</option>
            <option value="subtracao">-</option>
            <option value="multiplicacao">x</option>
            <option value="divisao">%</option>
          </select>
        </div>
        <div class="col-md-1">
          <input
            v-model="numero2"
            type="number"
            class="input-number form-control"
          />
        </div>
        <div class="row">
          <div class="col-md-3 mt-3">
            <input
              v-model="resultado"
              type="number"
              class="input-number form-control"
            />
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
.input-number::-webkit-inner-spin-button {
  -webkit-appearance: none;
}
.input-number {
  -moz-appearance: textfield;
}
</style>