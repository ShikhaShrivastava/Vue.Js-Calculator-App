<template>
  <div>
    <input
      type="number"
      placeholder="select first number"
      v-model.number="num1"
    />
    <select v-model="operation">
      <option value="add">+</option>
      <option value="sub">-</option>
      <option value="mul">*</option>
      <option value="div">/</option>
    </select>
    <input
      type="number"
      placeholder="select second number"
      v-model.number="num2"
    />
    <!--Display Output -->
    <h1>= {{ output }} </h1>
  </div>
</template>
<script>
export default {
  data() {
    return {
      operation: "",
      num1: 0,    //default took it as 0
      num2: 0,
    };
  },
  //Computed Properties for mathematical operation
  computed: {
    output() {
      switch (this.operation) {
        case "add":
          return this.num1 + this.num2;
        case "sub":
          return this.num1 - this.num2;
        case "mul":
          return this.num1 * this.num2;
        case "div":
          return this.num1 / this.num2;
      }
    },
  },
};
</script>
<style>
body{
    background-color: orangered;
}
input{
    margin: 0.5em;
    height: 20px;
    width: 150px;

}
h1{
    font-size: 25px;
    color:#000;
}
input select{
    width: 30px;
}
</style>
