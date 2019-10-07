<template>
    <div id="result">
        <div v-if="has_result" class="panel result">
            <div v-if="monster_life == 0" class="win">
                Você ganhou!!! :)
            </div>
            <div v-else class="lose">
                Você perdeu! :(
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>