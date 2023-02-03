<template>
  <component :is="icon" :class="`text-${color}`" />
</template>
<script lang="ts" setup>
import { defineAsyncComponent, onMounted } from 'vue';

interface Props {
  name: string;
  color?: string;
}

const props = withDefaults(defineProps<Props>(), { color: 'dark' });
const icon = defineAsyncComponent(
  () => import('../../assets/icons/' + `${props.name}.svg`)
);
</script>
<style lang="scss" scoped>
@each $key, $val in $colors-list {
  .#{'text-' + $key} {
    color: #{$val};
  }
}
</style>
