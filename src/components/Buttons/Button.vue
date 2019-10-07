<template>
    <div id="button">
        <!-- <button @click="attack(false)" class="btn attack"> -->
        <button :class="buttonClass">
            {{ button_role }}
        </button>
    </div>
</template>

<script>
    export default {
        name: 'app-button',
        props: {
            button_role: String,
            type: {
                type: String,
                default: "btn"
            }
        },
        computed: {
            buttonClass(){
                return `btn ${this.type}`
            }
        }
    }
</script>

<style>

    .btn{
        padding: 5px 10px;
        margin: 0px 10px;
        border-radius: 5px;
        text-transform: uppercase;
        font-size: 1.1rem;
    }

    .new-game{
        background-color: #4253af;
        color: #fff;
    }

    .attack{
        background-color: #e51c23;
        color: #fff;
    }

    .special-attack{
        background-color: #ff9800;
        color: #000;
    }

    .heal{
        background-color: #259b24;
        color: #fff;
    }

    .give-up{
        background-color: #bbb;
        color: #000;
    }
</style>