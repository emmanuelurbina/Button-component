<template>
  <div>
      <buttons-component :type="type" :color="color" :shadow="shadow" />
  </div>
</template>



<script>
import ButtonsComponent from "@/components/ButtonsComponent.vue"
export default {
  name: "ButtonsView",
  data() {
    return {
      type: "default",
      color: "primary",
      shadow: true,
    };
  },
  components: {
    "buttons-component": ButtonsComponent,
  },
};
</script>


