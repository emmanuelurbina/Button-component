<template>
  <div id="app" class="content">
    <ButtonsView />
  </div>
</template>

<script>
import ButtonsView from "./views/ButtonsView.vue"

export default {
  name: 'App',
  components: {
    ButtonsView
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
  
 justify-content: center;
}
</style>
