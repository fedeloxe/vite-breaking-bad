<script>

import { store } from '../store.js'

export default {
    data() {
        return {
            store,
            archetypes: [
                'Alien',
                'Cipher',
                'Dark Magician',
                'Laval',
                'Performapal',
                'Vylon',
                'Elemental HERO',

            ],
            selectedArc: ''
        }
    }

}
</script>
<template lang="">
    <div class="bg-orange">
        <div class="select-container">
            <select v-model="store.selectedArc" @change="$emit('select')" name="arc" id="arc"> 
                <option v-for="(item, index) in archetypes" :key="item" :value="item">{{ item }}</option>
            </select>
        </div>

    </div>
</template>
<style lang="scss" scoped>
.bg-orange {
    background-color: #d48f38;

    .select-container {
        padding: 30px 0;
        width: 80%;
        margin: 0 auto;
    }
}
</style>