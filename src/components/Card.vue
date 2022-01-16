<template>
    <div class="card">
        <div class="content-wrap">
            <div class="img-wrap">
                <img :src="require(`@/assets/images/${card.image}`)">
            </div>
            <h3>{{ card.title }}</h3>
            <p>{{ card.details }}</p>
        </div>
        <button class="btn-solid">{{ card.button_text }}</button>
    </div>
</template>

<script>
export default {
    props: ['card']
}
</script>

<style>
.card {
    width: 100%;
    max-width: 360px;
    margin: 0 auto;
}
.card h3, .card p {
    margin: 20px 0;
}

@media screen and (min-width: 680px) {
    .card {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .img-wrap {
        height: 200px;
        display: flex;
        justify-content: center;
    }
}
</style>