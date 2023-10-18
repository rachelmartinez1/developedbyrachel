<template>
    <div class="outer-border">
        <h1>Number Guessing Game</h1>
        <p v-if="isGameRunning">Guess a number {{ min }} - {{ max }}:</p>
        <input v-model="userGuess" type="number" @keyup.enter="checkGuess" v-if="isGameRunning">
        <p v-if="isGameRunning">Attempts: {{ attempts }}</p>
        <p v-if="isGameRunning">Message: {{ message }}</p>
        <button @click="startGame" v-if="!isGameRunning" class="new-game-btn">Start New Game</button>
        <button @click="resetGame" v-if="isGameRunning" class="reset-game-btn">Restart</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            min: 1,
            max: 10,
            targetNumber: 0,
            userGuess: null,
            attempts: 0,
            isGameRunning: false,
            message: "",
        }
    },
    methods: {
        startGame() {
            this.targetNumber = this.getRandomNumber();
            this.userGuess = null;
            this.attempts = 0;
            this.isGameRunning = true;
            this.message = "";
        },
        getRandomNumber() {
            return Math.floor(Math.random() * (this.max - this.min + 1)) + this.min;
        },
        checkGuess() {
            this.attempts++;
            if (this.userGuess == this.targetNumber) {
                this.message = `Congratulations! You guessed the number in ${this.attempts} attempts.`;
            } else if (this.userGuess < this.targetNumber) {
                this.message = "Try a higher number.";
            } else {
                this.message = "Try a lower number.";
            }
        },
        resetGame() {
            this.isGameRunning = false;
        }
    }
}
</script>

<style scoped>
.outer-border {
    border: 1px solid black;
    padding: 20px;
    width: 410px;
    margin: 0 auto;
}

.new-game-btn {
    margin-top: 20px;
}
</style>