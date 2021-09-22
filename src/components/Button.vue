<template>
    <button type="button" class="w3-button w3-blue"
        id="{{button.id}}">
        {{button.label}}
    </button>
</template>

<script>
export default {
    name: "Button",
    props: ["button"],
}
</script>