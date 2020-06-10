<template>
  <div id="app">
    <notes></notes>
  </div>
  
</template>
<script>
import 'semantic-ui-css/semantic.min.css'

import Notes from './components/Notes'


export default {
  name: 'App',
  components: {
    Notes
  }
  
}
</script>

<style scoped>
body{
    margin: 0;
    padding: 0;
}
.container{
    background: #fff;
    padding: 10px;
}
.item{
    box-shadow: 0 1px 1px rg(0,0,0,0.3);
    background: #fff;
    color: #ccc;
    padding: 30px;
    display: block;
    text-align: center;
}
.item span{
    font-size: 50px;
}
</style>
