<template>
  <div v-tooltip="tooltipValue" :style="{ backgroundColor: `var(--${value})` }"></div>
</template>

<script>
import mixin from "@directus/extension-toolkit/mixins/interface";

export default {
  mixins: [mixin],
  computed: {
    tooltipValue() {
      return this.value ? this.$helpers.formatTitle(this.value) : null;
    }
  }
};
</script>

<style lang="scss" scoped>
div {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 2px solid var(--white);
}
</style>
