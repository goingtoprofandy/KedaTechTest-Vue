<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div/>

  <form class="w3-container">
    <FieldRadio v-for="field in fields" :fieldRadio="field" :key="field" />
  </form>
</template>

<script>
import FieldRadio from "./components/FieldRadio.vue"

export default {
  name: 'App',
  components: {
    FieldRadio
  },
  data() {
    return {
      fields: [
        {value: "Inner Component", id: "radio-1", children: []},
        {value: "Radio B", id: "radio-2", children: []}
      ]
    }
  }
}
</script>