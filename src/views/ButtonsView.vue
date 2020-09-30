<template>
  <div>
    <div class="buttons">
      <buttons-component
        :type="type"
        :color="color"
        :shadow="shadow"
        :size="size"
        :iconLeftView="iconLeftView"
        :iconLeft="iconLeft"
        :iconRightView="iconRightView"
        :iconRight="iconRight"
      />
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
          <tr>
            <td>Box-Shadow</td>
            <td class="opt">
              <input type="checkbox" class="check" value="" v-model="shadow" />
            </td>
          </tr>
          <tr>
            <td>Icon Left</td>
            <td class="opt">
              <input
                type="checkbox"
                class="check"
                value=""
                v-model="iconLeftView"
              />
            </td>
          </tr>
          <tr>
            <td>Icon Left List</td>
            <td class="opt">
              <select class="select" @change="changeIconLeft">
                <option value="home" selected>Select Icon</option>
                <option
                  v-for="(icon, index) in iconList"
                  :key="index"
                  :value="icon"
                >
                  {{ icon }}
                </option>
              </select>
            </td>
          </tr>
          <tr>
            <td>Icon right</td>
            <td class="opt">
              <input
                type="checkbox"
                class="check"
                value=""
                v-model="iconRightView"
              />
            </td>
          </tr>
          <tr>
            <td>Icon right List</td>
            <td class="opt">
              <select class="select" @change="changeIconRight">
                <option value="home" selected>Select Icon</option>
                <option
                  v-for="(icon, index) in iconList"
                  :key="index"
                  :value="icon"
                >
                  {{ icon }}
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
      size: "md",
      iconLeftView: false,
      iconLeft: "",
      iconRightView: false,
      iconRight: "",
      iconList: ["thumb_up", "thumb_down", "favorite", "shopping_cart", "add"],
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
    changeIconLeft: function () {
      this.iconLeft = event.target.value;
    },
    changeIconRight: function () {
      this.iconRight = event.target.value;
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

.check {
  width: 20px;
  height: 20px;
}
@media screen and (max-width: 600px) {
  table {
    width: 100%;
  }
}
</style>


