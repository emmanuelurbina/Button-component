<template>

    <button type="button" class="btn" :class="[type, color, size, shadow ? 'shadow': '']">
      Button
    </button>
  
</template>

<script>
export default {
  name: "ButtonsComponent",
  props: ["type", "color", "shadow", "size"],
};
</script>

<style scoped>


/* class btn and shadow custom*/
.btn {
  border: none;
  cursor: pointer;
  outline: none;
  padding: 10px 15px; /* md default size */
  border-radius: 6px;
  font-weight: 500;
  font-size: 12px;
  font-family: "Noto Sans JP", sans-serif;
}
.shadow {
  box-shadow: 1px 1px 2px 0px rgba(0, 0, 0, 0.3);
}

/*Types:
Defaul
Outline
Text
*/

.default {
  background-color: #e0e0e0;
}

.outline {
  border: 1px solid #e0e0e0;
  background-color: #fff;
  color: #3f3f3f;
}

.text {
  border: none;
  background-color: #fff;
  color: #3f3f3f;
}

/* colors:
primary
secondary
default
danger
*/

/* primary */
.default.primary {
  background-color: #3d5afe;
  color: #fff;
}

.outline.primary {
  border: 1px solid #3d5afe;
  background-color: #fff;
  color: #3d5afe;
}

.text.primary {
  background-color: #fff;
  color: #3d5afe !important;
}

/* seconadry */

.default.secondary {
  background-color: #455a64;
  color: #ffffff;
}

.outline.secondary {
  border: 1px solid #455a64;
  background-color: #fff;
  color: #455a64;
}

.text.secondary {
  background-color: #fff;
  color: #455a64 !important;
}

/* danger */

.default.danger {
  background-color: #d32f2f;
  color: #fff;
}

.outline.danger {
  border: 1px solid #d32f2f;
  background-color: #fff;
  color: #d32f2f;
}

.text.danger {
  background-color: #fff;
  color: #d32f2f !important;
}

/* hover  */

.default:hover {
  background-color: #aeaeae !important;
}

.outline:hover {
  border: 1px solid #3f3f3f !important;
  background-color: #e0e0e0 !important;
  color: #3f3f3f !important;
}

.text:hover {
  border: none !important;
  background-color: #fff !important;
  color: #e0e0e0 !important;
}

/* colors hover */
.default:hover.primary {
  background-color: #0039cb !important;
  color: #fff !important;
}

.outline:hover.primary {
  border: 1px solid #3d5afe !important;
  background-color: #eaefff !important;
  color: #3d5afe !important;
}

.text:hover.primary {
  border: none;
  background-color: #fff !important;
  color: #0039cb !important;
}

/*secondary*/
.default:hover.secondary {
  background-color: #1c313a !important;
  color: #fff !important;
}

.outline:hover.secondary {
  border: 1px solid #1c313a !important;
  background-color: #455a64 !important;
  color: #fff !important;
}

.text:hover.secondary {
  border: none;
  background-color: #fff;
  color: #1c313a !important;
}

/*danger*/
.default:hover.danger {
  background-color: #9a0007 !important;
  color: #fff !important;
}

.outline:hover.danger {
  border: 1px solid #9a0007 !important;
  background-color: #d9a7a7 !important;
  color: #9a0007 !important;
}

.text:hover.danger {
  border: none;
  background-color: #fff;
  color: #9a0007 !important;
}

.btn:disabled {
  cursor: not-allowed;
  pointer-events: none;
  box-shadow: none;
}
.btn:disabled.default,
.btn:disabled.outline {
  background-color: #e0e0e0;
  color: #9e9e9e;
}
.btn:disabled.text {
  background-color: #fff;
  color: #9e9e9e !important;
}

/* sizing */

.sm {
  padding: 5px 10px;
}

.md {
  /* default size */
  padding: 10px 15px;
}

.lg {
  padding: 15px 25px;
}
</style>