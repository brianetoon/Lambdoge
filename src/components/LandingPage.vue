<template>
    <main>
        <div class="wrapper">
            <Hero />
            <About />
            <Mission />
            <Comic />
        </div>
        <Tokenomics />
    </main>
</template>

<script>
import Hero from './Hero.vue'
import About from './About.vue'
import Mission from './Mission.vue'
import Comic from './Comic.vue'
import Tokenomics from './tokenomics/Tokenomics.vue'

export default {
    components: { Hero, About, Mission, Comic, Tokenomics }
}
</script>

<style>
.wrapper {
    padding: 10px 25px;
    max-width: 1160px;
    margin: 0 auto;
}

@media screen and (min-width: 680px) {
    .wrapper {
        padding: 20px 30px;
    }
}

@media screen and (min-width: 960px) {
    .wrapper section {
        margin-bottom: 160px;
    }
}
</style>