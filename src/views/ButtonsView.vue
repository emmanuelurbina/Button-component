<template>
  <div>
    <div class="buttons">
      <buttons-component :type="type" :color="color" :shadow="shadow" :size="size" />
    </div>

    <div class="table-content">
      <table class="tbl">
        <thead>
          <th>Description</th>
          <th>-</th>
        </thead>
        <tbody>
          <tr>
            <td>Button Type</td>
            <td class="opt">
              <select class="select" @change="changeType">
                <option value="default" selected>Select type</option>
                <option
                  v-for="(type, index) in types"
                  :key="index"
                  :value="type"
                >
                  {{ type }}
                </option>
              </select>
            </td>
          </tr>
          <tr>
            <td>Button Color</td>
            <td class="opt">
              <select class="select" @change="changeColor">
                <option value="default" selected>Select Color</option>
                <option
                  v-for="(color, index) in colors"
                  :key="index"
                  :value="color"
                >
                  {{ color }}
                </option>
              </select>
            </td>
          </tr>
          <tr>
            <td>Button Size</td>
            <td class="opt">
              <select class="select" @change="changeSize">
                <option value="default" selected>Select Size</option>
                <option
                  v-for="size in sizes"
                  :key="size.index"
                  :value="size.index"
                >
                  {{ size.text }}
                </option>
              </select>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>


<script>
import ButtonsComponent from "@/components/ButtonsComponent.vue";

export default {
  name: "ButtonsView",
  data() {
    return {
      type: "default",
      color: "",
      shadow: true,
      size: 'md',
      types: ["default", "outline", "text"],
      colors: ["default", "primary", "secondary", "danger"],
      sizes: [
        { index: "sm", text: "Slim" },
        { index: "md", text: "Default" },
        { index: "lg", text: "Large" },
      ],
    };
  },
  components: {
    "buttons-component": ButtonsComponent,
  },
  methods: {
    changeType: function () {
      this.type = event.target.value;
    },
    changeColor: function () {
      this.color = event.target.value;
    },
    changeSize: function () {
      this.size = event.target.value;
    },
  },
};
</script>

<style scoped>
.buttons {
  display: flex;
  justify-content: center;
  margin: 5em auto;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
  width: 600px;
  border: 1px solid #f1f1f1;
}

tr:nth-child(even) {
  background-color: #f2f2f2;
}


th,
td {
  padding: 8px;
}
.opt {
    text-align: right;
}
.select {
  cursor: pointer;
  padding: 5px 10px;
  border: none;
  border-radius: 8px;
}

@media screen and (max-width: 600px) {
  table {
    width: 100%;
  }
}
</style>


