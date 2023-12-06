<script setup>
import SeriesItem from './SeriesItem.vue';

    defineProps(['seriesList'])
</script>

<template>
    <div class="cards-list">
        <article v-for='series in seriesList'>
            <SeriesItem :series="series" />
        </article>
    </div>
</template>
<style scoped>
    .cards-list {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }
    article {
        width: 320px;
    margin: 15px;
    border: 2px solid #000;
    }

    @media screen and (max-width: 500px) {
        
    .cards-list {
        flex-direction: column;
        padding: 15px;
    }
    article {
        width: 100%;
        margin: unset;
    }
    }
</style>