<script>
import AppCardList from './AppCardList.vue';
import AppResultsMessage from './AppResultsMessage.vue';

export default {
    components: {
        AppCardList,
        AppResultsMessage,

    }

}
</script>
<template>
    <main>

        <div class="container">
            <AppResultsMessage />
            <AppCardList />

        </div>

    </main>

</template>


<style lang="scss" scoped >
main {
    background-color: #d48f38;
    width: 100%;

    .select {
        width: 80%;
        margin: 0 auto;
        padding: 20px 0;
    }


    .container {

        background-color: white;


        .select {
            padding: 20px;
            width: 200px;
        }

    }
}
</style>