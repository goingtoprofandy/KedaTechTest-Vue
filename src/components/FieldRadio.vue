<template>
    <input type="radio"
    class="w3-radio w3-margin-top"
    id="{{fieldRadio.id}}"
    value="{{fieldRadio.value}}"
    name="fieldRadioModel" />
    <label class="w3-margin-left" for="{{fieldRadio.id}}">
        {{fieldRadio.value}}
        <div v-for="itemChildren in fieldRadio.children" :key="itemChildren"
        class="w3-margin-left w3-margin-top" style="width: 256px !important">
            <div v-if="(itemChildren.type == 'FieldEditText')">
                <FieldEditText :fieldEditText="itemChildren"/>
            </div>
            <div v-if="(itemChildren.type == 'FieldEditDate')">
                <FieldEditDate :fieldEditDate="itemChildren"/>
            </div>
            <div v-if="(itemChildren.type == 'Button')">
                <Button :button="itemChildren"/>
            </div>
        </div>
    </label>
    
</template>

<script>
import FieldEditText from "./FieldEditText.vue"
import FieldEditDate from "./FieldEditDate.vue"
import Button from "./Button.vue"

export default {
    name: "FieldRadio",
    props: ["fieldRadio"],
    components: {
        FieldEditText,
        FieldEditDate,
        Button
    }
}
</script>