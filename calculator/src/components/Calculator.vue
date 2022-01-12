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

  .calculator{
    width: 375px;
    height: 800px;
    background: #1F1F1F;
    padding: 24px;
    border-radius: 30px;
  }
  .workArea{
    height: 350px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .tabBar{
    margin-top: 60px;
    color: #FFFFFF;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .calculation{
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
  .operation{
    font-family: 'Poppins', sans-serif;
    font-weight: 500;
    font-size: 28px;
    text-align: right;
    color: #AAAAAA;
  }
  .result{
    font-family: 'Poppins', sans-serif;
    font-weight: 500;
    font-size: 48px;
    text-align: right;
    color: #FFFFFF;
    margin-bottom: 12px;
  }
  
</style>
