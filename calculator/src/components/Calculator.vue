<template>
  <div class="calculator">
    <div class="workArea">
      <div class="tabBar">
        <i class="fas fa-calculator calc"></i>
        <i class="fas fa-ellipsis-v dots"></i>
      </div>
      <div class="calculation">
        <div class="operation">{{ history }}</div>
        <div class="result"> {{ current || 0 }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data: () => ({
    previous: '',
    current: '',
    operator: '',
    history: '',
  }),
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
