<template>
    <label v-if="fieldEditDate.label != null">{{fieldEditDate.label}}</label>
    <input
        class="w3-input w3-border" type="date" 
        id="{{fieldEditDate.id}}"
        name="{{fieldEditDate.name}}" />
</template>

<script>
export default {
    name: "FieldEditDate",
    props: ["fieldEditDate"],
}
</script>