<template>
    <div id="panel-score" :class="panelClass">
        <score character_role="Player" />
        <score character_role="Monster  " />
    </div>
</template>

<script>

import Score from './Score'

export default {
    name: 'panel-score',
    components: {
        Score
    },
    props: {
        type: String
    },
    computed: {
        panelClass(){
            return `${this.type}`;
        }
    }
}
</script>

<style>

    /* Área dos pontos */

    .scores{
        display: flex;
    }

</style>