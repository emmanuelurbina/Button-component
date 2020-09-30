<template>
  <div id="app" class='content'>
    <buttons-component :type='type' :color="color" :shadow="shadow"  />
  </div>
</template>

<script>
import ButtonsComponent from "./components/ButtonsComponent.vue"

export default {
  name: 'App',
  data(){
    return {
      type: "default",
      color:"primary",
      shadow: true
    }
  },
  components: {
    'buttons-component': ButtonsComponent
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  
}

.content {
  display: flex;
}
</style>
