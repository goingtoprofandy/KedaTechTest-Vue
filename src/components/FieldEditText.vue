<template>
    <input type="text" 
        id="{{fieldEditText.id}}"
        name="{{fieldEditText.name}}"
        class="w3-input w3-border" />
    <label v-if="fieldEditText.label != null">{{fieldEditText.label}}</label>
</template>

<script>
export default {
    name: "FieldEditText",
    props: ["fieldEditText"],
}
</script>