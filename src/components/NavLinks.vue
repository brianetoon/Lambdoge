<template>
    <nav>
        <ul class="nav-links">
            <!-- <li><a href="#hero">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#mission">Mission</a></li>
            <li><a href="#comic">Comic & NFT</a></li>
            <li><a @click="scrollTest">Tokenomics</a></li> -->

            <li v-for="(link, i) in links" :key="i">
                <a @click="scrollTest(link.anchor)">{{ link.name }}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
import gsap from 'gsap'
import ScrollToPlugin from 'gsap/ScrollToPlugin.js'
import { ref } from '@vue/runtime-core'

export default {
    setup() {
        const links = ref([
            { name: 'Home', anchor: '#hero'},
            { name: 'About', anchor: '#about'},
            { name: 'Mission', anchor: '#mission'},
            { name: 'Comic & NFT', anchor: '#comic'},
            { name: 'Tokenomics', anchor: '#tokenomics'},
        ])

        gsap.registerPlugin(ScrollToPlugin)

        const scrollTest = (anchor) => {
            gsap.to(window, {duration:.5, scrollTo:{y: anchor, offsetY: 340}})
            // console.log(anchor)
        }

        return { links, scrollTest }
    }
}
</script>

<style>

</style>