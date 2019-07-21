<template>
    <div class="calculator">
        <screen class="screen" :inputValue="keyFormation.join('')"></screen>
        <keyboard @pressedKey="RecivedKey" ></keyboard>
    </div>
</template>

<script>
import Keyboard from './Keyboard';
import Screen from './Screen';

export default {
    data () {
        return {
            PressedKey: '',
            keyFormation: []

        }
    },
    components: {
        Keyboard, Screen
    },
    methods: {
        RecivedKey (key) {
            this.PressedKey = key;
            this.keyFormation.push(key);
        }
    }
}
</script>

<style>
    .calculator {
        display: grid;
        place-content: center;
    }
    .screen {
        background-color: goldenrod;
        padding: 28px;
    }
</style>
