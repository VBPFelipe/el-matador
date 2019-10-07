<template>
    <div id="panel-score" :class="panelClass">
        <score character_role="Player" character_life.name="player_life"/>
        <score character_role="Monster" character_life.name="monster_life"/>
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