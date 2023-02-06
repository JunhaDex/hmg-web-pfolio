<template>
  hello world!
  <p>{{ foo }}</p>
  <Icon name="activity" />
  <v-btn elevation="2">click me!</v-btn>
</template>
<script lang="ts" setup>
import Icon from '@/components/utils/Icon.vue';

const foo = 'foo';
</script>
<style lang="scss">
.icon {
  display: inline-block;
  color: #00adb5;
}
</style>
