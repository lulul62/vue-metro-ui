<template>
 <span :class="this.class"><slot>{{this.badge}}</slot></span>
</template>
<script>
export default {
  name: "tileBadge",
  props: ["badge"],
  data() {
    return {
      class: ["tile-badge"]
    };
  }
};
</script>

<style>

</style>