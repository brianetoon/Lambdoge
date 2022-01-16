<template>
    <section id="about">
        <h2>About Lambdoge</h2>
        <div class="cards">
            <Card v-for="(card, i) in cards" :key="i" :card="card"/>
        </div>
    </section>
</template>

<script>
import store from '@/store.js'
import { ref } from '@vue/reactivity'
import Card from './Card.vue'

export default {
    components: { Card },
    setup() {
        const cards = ref(store.about)

        return { cards }
    }
}
</script>

<style>
#about {
    margin-bottom: 100px;
}
.cards {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: 10px;
    margin: 20px auto;
}
.card {
    grid-column: span 12;
}

@media screen and (min-width: 680px) {
    .cards {
        gap: 20px;
        margin: 40px auto;
    }
    .card {
        grid-column: span 6;
    }
    .card:last-child {
        grid-column: 4/10;
    }
}

@media screen and (min-width: 960px) {
    .cards {
        gap: 40px;
        max-width: 1160px;
    }
    .card {
        grid-column: span 4;
    }
    .card:last-child {
        grid-column: 9/13;
    }
}

@media screen and (min-width: 1200px) {
    .cards {
        gap: 60px;
    }
}
</style>