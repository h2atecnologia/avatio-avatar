<template>
  <component :is="typeComponent" :color="color"/>
</template>

<script>
import TypeA from "../Common/Accessory/TypeA";
import TypeB from "../Common/Accessory/TypeB";
import UseColor from "../Mixins/UseColor";

export default {
  mixins: [UseColor],
  components: { TypeA, TypeB },
  props: {
    type: {
      type: String,
      default: "A"
    }
  },
  computed: {
    typeComponent() {
      return "Type" + this.type;
    }
  }
};
</script>
