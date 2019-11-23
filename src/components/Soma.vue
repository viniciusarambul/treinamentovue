<template>
  <div>
    <input v-model="a" type="number">
    <input v-model="b" type="number">
    <p>Resultado: {{ result }}</p>
  </div>
</template>

<script>
export default {
  props: {
    a: {
      type: Number,
      required: true,
      default: 30
    },
    b: Number
  },
  computed: {
    result: function() {
      return parseInt(this.a) + parseInt(this.b)
    }
  }
}
</script>

<style>
p {
  color: #333;
  border-radius: 5px;
  padding: 10px 40px;
  width: 100%;
  text-align: center;
  background: #CCC
}
input {
  box-sizing: border-box;
  background: #eee;
  border-radius: 5px;
  padding: 10px 40px;
  width: 100%;
  border: 1px solid #CCC;
  margin: 5px 0;
}
</style>
