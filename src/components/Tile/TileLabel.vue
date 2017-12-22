<template>
 <span :class="this.class"><slot>{{this.label}}</slot></span>
</template>
<script>
export default {
  name: "tileLabel",
  props: ['label'],
  data() {
    return {
      class: ["tile-label"]
    };
  }
};
</script>

<style>

</style>