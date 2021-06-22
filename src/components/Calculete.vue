<template>
  <div class="hello">
    <h1>{{ msg }} {{ c }}</h1>
    <input v-model.number="operand1" />
    <input v-model.number="operand2" />
    <div>
      <button @click="calc('+')">+</button>
      <button @click="calc('-')">-</button>
      <button @click="calc('/')">/</button>
      <button @click="calc('/0')">/0</button>
      <button @click="calc('*')">*</button>
      <button @click="calc('№')">x</button>
    </div>
    <h1>Ответ:{{ result }}</h1>
  </div>
</template>

<script>
export default {
  name: "Calculete",
  data: () => ({
    operand1: 0,
    operand2: 0,
    result: 0,
  }),
  props: {},
  methods: {
    calc(op) {
      const { operand1, operand2 } = this;
      const calcOperation = {
        "+": () => operand1 + operand2,
        "-": () => operand1 - operand2,
        "/": () => operand1 / operand2,
        "*": () => operand1 * operand2,
        "№": () => Math.pow(operand1, operand2),
        "/0": () => Math.floor(operand1 / operand2),
      };
      this.result = calcOperation[op]();
    },
  },
};
</script>

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
