<template>
  <div id="app">
    
    <panel-score type="panel scores"/>

    <!-- <panel-result /> -->
    
    <panel-buttons type="panel buttons"/>
<!-- 
    <panel-logs />
 -->
  </div>
</template>

<script>
import PanelScore from './components/Scores/PanelScore'
import PanelButtons from './components/Buttons/PanelButtons'

export default {
  name: 'app',
  components: {
    PanelScore, PanelButtons
  }
}
</script>

<style>
  #app{
      /* orientação por coluna */
      display: flexbox;
      flex-direction: column;
      font-family: 'Montserrat', sans-serif;
  }

  .panel {
      margin: 10px;
      padding: 20px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
  }
</style>
