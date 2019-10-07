<template>
    <div id="panelButtons" :class="panelClass">
        <app-button type="attack" button_role="Ataque" @click="attack(false)" />
        <app-button type="special-attack" button_role="Ataque Especial" @click="attack(true)" />
        <app-button type="heal" button_role="Cura" @click="heal_and_hurt" />
        <app-button type="give-up" button_role="Desiste" />
    </div>
</template>

<script>
import AppButton from "./Button";
import Score from "@/components/Scores/Score";

export default {
    name: "panel-buttons",
    components: {
        AppButton
    },
    props: {
        type: {
        type: String,
        default: "panel"
        }
    },
    computed: {
        panelClass() {
        return `${this.type}`;
        }
    },
    methods: {
        attack(special) {
            console.log("Alguma coisa");
            var atr = character_life.name["monster_life"];

        // this.hurt('monster_life', 5, 10, special,
        //     'Player', 'Monster'
        //     // , 'player'
        // )
        // if(this.monster_life > 0)
        //     this.hurt('player_life', 7, 12, false,
        //         'Monster', 'Player'
        //         // , 'monster'
        //     )
        },
        hurt(
        atr,
        min,
        max,
        special,
        source,
        target
        // ,cls
        ) {
        const plus = special ? 5 : 0;
        const hurt = this.get_random(min + plus, max + plus);
        //this[prop] - acessa em this o nome da variável
        this[atr] = Math.max(this[prop] - hurt, 0);
        // this.register_log(
        //     `${source} atingiu ${target} com ${hurt}.`, cls
        // )
        },
        heal_and_hurt() {
        this.heal(10, 15);
        this.hurt(
            "player_life",
            7,
            12,
            false,
            "Monstro",
            "Jogador"
            // , 'monster'
        );
        },
        heal(min, max) {
        const heal = this.get_random(min, max);
        this.player_life = Math.min(this.player_life + heal, 100);
        // this.register_log(
        //     `Jogador ganhou força de ${heal}.`, 'player'
        // )
        }
    }
};
</script>

<style>
.buttons {
    display: flex;
    justify-content: center;
}
</style>