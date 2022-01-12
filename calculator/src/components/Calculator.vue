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
    <div class="buttonsArea">
      <div class="buttonColumn">
        <div @click="clear" class="buttonCalc clearButton">c</div>
        <div @click="pushNumber('7')" class="buttonCalc">7</div>
        <div @click="pushNumber('4')" class="buttonCalc">4</div>
        <div @click="pushNumber('1')" class="buttonCalc">1</div>
        <div class="buttonCalc"></div>
      </div>
      <div class="buttonColumn">
        <div @click="backSpace" class="buttonCalc backButton"><i class="fas fa-backspace"></i></div>
        <div @click="pushNumber('8')" class="buttonCalc">8</div>
        <div @click="pushNumber('5')" class="buttonCalc">5</div>
        <div @click="pushNumber('2')" class="buttonCalc">2</div>
        <div @click="pushNumber('0')" class="buttonCalc">0</div>
      </div>
      <div class="buttonColumn">
        <div @click="percentage" class="buttonCalc operation"><i class="fas fa-percentage"></i></div>
        <div @click="pushNumber('9')" class="buttonCalc">9</div>
        <div @click="pushNumber('6')" class="buttonCalc">6</div>
        <div @click="pushNumber('3')" class="buttonCalc">3</div>
        <div @click="pushNumber('.')" class="buttonCalc">.</div>
      </div>
      <div class="buttonColumn">
        <div @click="divide" class="buttonCalc operation"><i class="fas fa-divide"></i></div>
        <div @click="multiply" class="buttonCalc operation" ><i class="fas fa-times"></i></div>
        <div @click="subtract" class="buttonCalc operation"><i class="fas fa-minus"></i></div>
        <div @click="add" class="buttonCalc operation"><i class="fas fa-plus"></i></div>
        <div @click="finalResult" class="buttonCalc operation equalButton"><i class="fas fa-equals"></i></div>
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
  .buttonsArea{
    padding-top: 20px;
    border-top: 1px solid #5A5A5A;
    height: 400px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .buttonColumn{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .buttonCalc{
    font-family: 'Poppins', sans-serif;
    font-weight: normal;
    font-size: 32px;
    height: 60px;
    width: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #FFFFFF;
    cursor: pointer;
  }
  .equalButton{
    background: #FF762D;
    border-radius: 18px;
  }
  .clearButton, .backButton{
    color: #FF762D;
  }
  .backButton, .operation{
    font-size: 24px;
  }
  .calc{
    font-size: 40px;
  }
  .dots{
    font-size: 20px;
  }
</style>
