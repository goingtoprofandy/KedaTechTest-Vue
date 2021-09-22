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
        {value: "Inner Component", id: "radio-1", children: [
          {
            type: "FieldEditText",
            id: "field-edit-text-1",
            name: "fieldEditText1"
          },
          {
            type: "FieldEditDate",
            id: "field-edit-date-1",
            name: "fieldEditDate1",
            label: "Choose A Date"
          }
        ]},
        {value: "Radio B", id: "radio-2", children: [
          {
            type: "Button",
            id: "button-submit",
            label: "Button Submit"
          }
        ]}
      ]
    }
  }
}
</script>