<template>
    <div class="big-button">
        <span ref="bigbuttontext"></span>
    </div>
</template>

<script>
import TypeIt from "typeit";

export default {
    mounted() {
        const text = this.$refs['bigbuttontext']

        const typer = new TypeIt(text, {
            afterComplete: () => {
                // some animations to make here
            }
        })

        typer
            .type('Be Eternal')
            .pause(750)
            .delete(7)
            .type('Immortal')
            .pause(750)
            .delete(8)
            .type('Ordinal')
            .pause(1250)
            .delete(11)
            .type("Ordinal Board")

        typer.go()
    },
}
</script>

<style lang="scss">
.big-button {
    display: inline-block;
    box-sizing: border-box;
    border: none;
    outline: none;
    position: relative;
    z-index: 0;
    border-radius: 2px;
    padding: 0 10px;
    color: $primaryColor;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    font-size: 22px;
    width: 100%;
    height: 42px;
    line-height: 42px;
    text-align: center;
}

.big-button::before {
}

.big-button:hover {
    text-decoration: underline;
    color: $primaryColor !important;
}

.big-button:hover:before {
    background: $primaryColor !important;
}

.big-button::after {
    z-index: -1;
    content: '';
    position: absolute;
    width: calc(100% + 20px);
    height: calc(100% + 20px);
    background: #111;
    left: -10px;
    top: -10px;
    border-radius: 2px;
}

@keyframes glowing {
    0% {
        background-position: 0 0;
    }

    50% {
        background-position: 400% 0;
    }

    100% {
        background-position: 0 0;
    }
}
</style>