<template>
    <nav>
        <ul class="nav-links">
            <li v-for="(link, i) in links" :key="i">
                <a @click="scrollTest(link.anchor)">{{ link.name }}</a>
            </li>
            <li class="ldoge">
                <a href="https://rocketswap.exchange/#/swap/con_lambdoge" target="_blank">
                    Buy $LDOGE
                </a>
            </li>
        </ul>
    </nav>
</template>

<script>
import gsap from 'gsap'
import ScrollToPlugin from 'gsap/ScrollToPlugin.js'
import { ref } from '@vue/runtime-core'

export default {
    setup(props, { emit }) {
        const links = ref([
            { name: 'Home', anchor: '#hero'},
            { name: 'About', anchor: '#about'},
            { name: 'Mission', anchor: '#mission'},
            { name: 'Comic & NFT', anchor: '#comic'},
            { name: 'Tokenomics', anchor: '#tokenomics'},
        ])

        const close = () => {
            emit('close')
        }

        gsap.registerPlugin(ScrollToPlugin)

        const scrollTest = (anchor) => {
            gsap.to(window, {duration:.5, scrollTo:{y: anchor, offsetY: 100}, onComplete:close})
        }

        return { links, scrollTest }
    }
}
</script>

<style>
.ldoge {
    display: none;
}
.ldoge a {
    color: var(--primary);
    background: var(--lambdoge);
    padding: 10px 15px;
    font-weight: 700;
    border-radius: 50px;
}
.ldoge a:hover {
    color: var(--primary);
    background: white;
}
@media screen and (min-width: 1200px) {
    .ldoge {
        display: block;
    }
}
</style>