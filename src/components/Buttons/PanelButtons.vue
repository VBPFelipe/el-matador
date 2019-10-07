<template>
    <div id="panelButtons" :class="panelClass">
        <app-button type="attack" button_role="Ataque"/>
        <app-button type="special-attack" button_role="Ataque Especial"/>
        <app-button type="heal" button_role="Cura"/>
        <app-button type="give-up" button_role="Desiste"/>
    </div>
</template>

<script>
import AppButton from './Button'

export default {
    name: 'panel-buttons',
    components:{
        AppButton
    },
    props:{
        type: {
            type: String,
            default: 'panel'
        }
    },
    computed: {
        panelClass(){
            return `${this.type}`
        }
    }
}
</script>

<style>
    .buttons {
        display: flex;
        justify-content: center;
    }
</style>