<script setup>
    defineProps(['series'])
</script>

<template>
    <div class="card">
        <div class="img-container">
            <img :src="series.poster" alt="poster">
        </div>
        <div class="content">
            <h3 class="name">{{ series.web_series_name }}</h3>
        <p class="date"><span>{{ series.aired_date }}</span> | <span>{{ series.number_of_seasons_and_episodes }}</span></p>
        <p class="genre">{{ series.genre  }}</p>
        <div class="actions">
            <p class="rating">{{ series.rating  }}</p>
            <a target="_blank" :href="series.reference_url"><span><i class="fa fa-arrow-circle-right" aria-hidden="true"></i></span></a>
        </div>
        </div>
    </div>
</template>

<style scoped>
    .img-container{
        height: 250px;
    }
    .img-container img{
        width: 100%;
        height: 100%;
    }
    .name {
        font-weight: bold;
    padding: 10px 0;
    }
    p{
        margin-bottom: 10px;
        font-size: 14px;
    }
    .actions{
        display: flex;
        justify-content: space-between;
    }
    span i{
        padding: 0 10px;
    }
    .content {
        padding: 0 10px;
    }
    a {
        text-decoration: none;
        color: #8d1111;
    }
</style>