<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps({
  name: {
    type: String,
    required: true,
  }
})

const symbolId = computed(() => `#icon-${props.name}`)


</script>

<script lang="ts">
export default {
  name:'SvgIcon'
}
</script>

<template>
  <svg aria-hidden="true" class="svg-icon">
    <use :xlink:href="symbolId" fill="currentColor" />
  </svg>
</template>

<style lang="scss" scoped>
.svg-icon {
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>