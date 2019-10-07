<template>
    <div id="score" class="score">
        <h1>{{ character_role }}</h1>
        <div class="life-bar">
            <div class="life"
                :class="{danger : character_life < 20}"
                :style="{width: character_life + '%'}">
            </div>
        </div>
        <div>{{ character_life }}%</div>
    </div>
</template>

<script>
export default {
    name: 'score',
    props: {
            character_role: String,
            character_life: {
                type: Number,
                default: 100
            }
    }
}
</script>

<style>

    .score{
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .score h1{
        font-weight: 300;
        font-size: 1.6rem
    }

    .life-bar{
        width: 80%;
        height: 20px;
        border: 1px solid #AAA;
    }

    .life-bar .life{
        display: flex;
        justify-content: center;
        height: 100%;
        background-color: green;
    }

    .life-bar .life.danger{
        background-color: red;
    }
</style>