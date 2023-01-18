<script>
import { store } from '../store.js';
export default {
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <div class="cont">
        <h4>Trovati {{ store.cards.length }} risultati</h4>
    </div>


</template>
<style lang="scss" scoped>
.cont {
    padding: 20px;
    background-color: black;

    h4 {
        color: white;
    }
}
</style>