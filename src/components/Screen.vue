<template>
    <div>
        {{inputValue}}
    </div>
</template>

<script>
export default {
    props: {
        inputValue: String
    },
    mounted() {
        this.$emit('reciveInput', (key) => {
            console.log("sdfs sdvsd" + key)
        })
    }
}
</script>

<style>

</style>
