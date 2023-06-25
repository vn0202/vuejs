<template>
    <div class="ui message" :class="type" v-show="!hidden">
        <i class="close icon" @click="hide"></i>
        <div class="header">
            {{ header }} </div>
            <slot></slot>
    </div>
</template>
<script>
export default {
    data() {
        return {
            hidden: false,
        }
    },
    props: {
        type: {
            type: String,
            required: false,
            default: "info",
        },
        header: {
            type: String,
            required: true,
            default:"The default header"
        }
    },
    methods: {
        hide()
        {
            return this.hidden = true;
        }
    },
}
</script>
<style></style>