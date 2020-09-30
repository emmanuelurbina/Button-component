<template>
  <div id="app" class="content">
    <ButtonsView />


    <div class="footer">
      <p>
        <a class="flink" href="https://emmanuelurbina.github.io">Emmanuel Lucio Urbina </a> <br>
        <a class="flink" href="https://devchallenges.io/"> @devchallenges.io </a>
       </p>
    </div>
  </div>
</template>

<script>
import ButtonsView from "./views/ButtonsView.vue";

export default {
  name: "App",
  components: {
    ButtonsView,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.content {
  display: grid;

  justify-content: center;
}



.footer {
  position: absolute;
  bottom: 0;
  padding: 1em;
  text-align: center;
  width: 100%;
  font-size: 22px;
  font-weight: bold;
  color: tomato;
}

.flink {
  text-decoration: none;
  color: tomato;
}

@media screen and (max-width: 600px)  {
  .footer {
    position: relative;
    font-size: 16px;
  }
}
</style>
