<template>
    <section id="about">
        <h2>About Lambdoge</h2>
        <div class="cards grid">
            <Card v-for="(card, i) in cards" :key="i" :card="card" class="grid-item"/>
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

@media screen and (min-width: 960px) {
    #about .grid {
        gap: 40px;
    }
}

@media screen and (min-width: 1200px) {
    #about .grid {
        gap: 60px;
    }
}
</style>