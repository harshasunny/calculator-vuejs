<template>
    <div class="keyboard">
        <div class="kb_button" v-for="key in Keys" :key="key" @click="KeyPress(key)">{{key}}</div>

        <div @click="addNumber(1)">1</div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            NumberKeys: [],
            Keys: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0', '+', '-', '*', '=', 'Clear', '/']
        }
    },
    methods: {
        KeyPress (key) {
            this.$emit('pressedKey', key);
        },
        addNumber (num) {
            this.NumberKeys.push(num); 
        }
    }
}
</script>

<style>
    .keyboard {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        width: 600px;
    }
    .kb_button {
        display: grid;
        height: 50px;
        place-content: center;
        background-color: coral;
        border: 1px solid black;
    }
</style>
