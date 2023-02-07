<template>
  <div class="counter">
    <button id="btn-remote" v-on:click="count+=3">
      <slot>remote-simple's Button: {{ count }}</slot>
    </button>
  </div>
</template>

<script lang="ts">
import {Vue, Component} from "vue-property-decorator";

@Component
export default class Counter extends Vue {
  public count: number = 0;
}
</script>

<style scoped>

</style>
