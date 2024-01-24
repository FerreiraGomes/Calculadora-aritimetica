<script setup></script>

<template>
  <div class="container">
    <header class="p-5 mb-4 mt-4">
      <h1>Calculadora Arítimetica</h1>
      <p>Você poderá fazer várias contas utilizando essa calculadora</p>
    </header>
    <form class="text-center">
      <div class="row">
        <div class="col-md-1">
          <input type="number" class="form-control" />
        </div>
        <div class="col-md-1">
          <select class="form-control text-center">
            <option value="adicao">+</option>
            <option value="subitracao">-</option>
            <option value="multiplicacao">x</option>
            <option value="divisao">%</option>
          </select>
        </div>
        <div class="col-md-1">
          <input type="number" class="form-control" />
        </div>
        <div class="row">
          <div class="col-md-3 mt-3">
            <input type="number" class="form-control" />
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped></style>
