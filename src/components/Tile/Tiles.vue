<template>
<div :class="this.class.join('')">
     <tile-content>
         <tile-label :label="this.label"></tile-label>
           <tile-badge :badge="this.badge"></tile-badge>
           </tile-content>
</div>
</template>
  
<script>
import TileContent from "./TileContent";
import TileLabel from "./TileLabel";
import TileBadge from "./TileBadge";
export default {
  name: "tile",
  props: ["small", "wide", "large", "label", "badge"],
  components: {
    TileContent,
    TileLabel,
    TileBadge
  },
  data() {
    return {
      class: ["tile-"]
    };
  },
  mounted() {
    this.initComponent();
  },
  methods: {
    initComponent() {
      const lockSize = ["small", "wide", "large"];
      Object.keys(this.$props).forEach(key => {
        if (lockSize.includes(key)) {
          if (this.$props[key] !== undefined) this.class.push(key);
        }
      });
    }
  }
};
</script>

<style>

</style>
