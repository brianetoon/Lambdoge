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
    padding: 10px 25px;
    max-width: 1160px;
    margin: 0 auto;
}
@media screen and (min-width: 680px) {
    main {
        padding: 20px 30px;
    }
}
</style>