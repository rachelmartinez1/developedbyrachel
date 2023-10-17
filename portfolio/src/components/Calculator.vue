<template>
    <div class="calculator">
        <input type="text" class="display" v-model="display" readonly>
        <div class="buttons">
            <button v-for="button in buttons" :key="button.value" @click="appendToDisplay(button.value)">{{ button.label }}</button>
            <button @click="clearDisplay" class="clear">C</button>
            <button @click="calculateResult" class="equal">=</button>
        </div>
    </div>
</template>
    <script>
    export default {
        data() {
        return {
            display: '',
            buttons: [
                { label: '1', value: '1' },
                { label: '2', value: '2' },
                { label: '3', value: '3' },
                { label: '+', value: '+' },
                { label: '4', value: '4' },
                { label: '5', value: '5' },
                { label: '6', value: '6' },
                { label: '-', value: '-' },
                { label: '7', value: '7' },
                { label: '8', value: '8' },
                { label: '9', value: '9' },
                { label: '*', value: '*' },
                { label: '0', value: '0' },
                { label: '/', value: '/' },
            ],
        }
    },
        methods: {
            appendToDisplay(value) {
                this.display += value;
            },
            clearDisplay() {
                this.display = '';
            },
            calculateResult() {
                try {
                    this.display = eval(this.display);
                } catch (error) {
                    this.display = 'Error';
                }
            },
        }
    }
    </script>

    <style lang="scss" scoped>
        body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 300vh;
        margin: 0;
        background-color: #f0f0f0;
    }

    .calculator {
        background-color: #f5f5f5;
        border: 1px solid #ccc;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        display: flex;
        flex-direction: column;
        width: 400px;
    }

    .display {
        font-size: 24px;
        text-align: right;
        padding: 10px;
        border: none;
        outline: none;
        border-top-left-radius: 8px;
        border-top-right-radius: 8px;
    }

    .buttons {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 1px;
    }

    button {
        background-color: #444;
        color: #fff;
        font-size: 50px;
        border: none;
        outline: none;
        cursor: pointer;
    }

    button.clear {
        background-color: #c80dbb;
    }

    button.equal {
        background-color: #54d813;
    }
</style>

