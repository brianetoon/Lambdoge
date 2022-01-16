<template>
    <main>
        <Hero />
        <About />
        <Mission />
        <Comic />
        <Tokenomics />
    </main>
</template>

<script>
import Hero from './Hero.vue'
import About from './About.vue'
import Mission from './Mission.vue'
import Comic from './Comic.vue'
import Tokenomics from './Tokenomics.vue'

export default {
    components: { Hero, About, Mission, Comic, Tokenomics }
}
</script>

<style>
main {
    padding: 15px;
}
@media screen and (min-width: 680px) {
    main {
        padding: 30px;
    }
}
</style>