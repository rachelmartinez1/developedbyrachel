<template>
    <div class="typing-carousel">
        <h1>Coming {{ currentText }}</h1>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            texts:[
                    "today...",
                    "tomorrow...",
                    "soon!",
                ],
                currentText: " ",
                textIndex: 0,
                typingSpeed: 100 // in milliseconds
            }
        },
        created() {
                this.startTyping();
        },
        methods: {

            startTyping() {
                    const text = this.texts[this.textIndex];
                    let charIndex = 0;

                    const typingInterval = setInterval(() => {
                        if (charIndex < text.length) {
                            this.currentText = text.slice(0, charIndex + 1);
                            charIndex++;
                        } else {
                            clearInterval(typingInterval);

                            setTimeout(() => {
                                this.eraseText();
                            }, 1500); // Pause before erasing
                        }
                    }, this.typingSpeed);
                },
                eraseText() {
                    let charIndex = this.currentText.length;

                    const erasingInterval = setInterval(() => {
                        if (charIndex > 0) {
                            this.currentText = this.currentText.slice(0, charIndex - 1);
                            charIndex--;
                        } else {
                            clearInterval(erasingInterval);

                            this.textIndex = (this.textIndex + 1) % this.texts.length;
                            setTimeout(() => {
                                this.startTyping();
                            }, 500); // Pause before starting the next text
                        }
                    }, this.typingSpeed);
                },
            },
    }
</script>