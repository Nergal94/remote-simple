<template>
  <div>
    <button :class="$style.button" id="btn-remote" v-on:click="count+=2">
      <slot>remote-simple's Button: {{ count }}</slot>
    </button>
    <counter />
  </div>
</template>

<script lang="ts">
import {Vue, Component} from "vue-property-decorator";
import Counter from './Counter.vue';

@Component({
  components: {
    Counter
  }
})
export default class Button extends Vue {
  public count: number = 0;
}
</script>
<style module>
.button {
  background-color: #4caf50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</style>
