<template>
<div :class="this.class"><slot></slot></div>
</template>
<script>
export default {
  name: 'tileContent',
  props: ['message'],
  data() {
    return {
      class: ['tile-content']
    };
  },
  mounted() {},
  methods: {}
};
</script>

<style>

</style>
