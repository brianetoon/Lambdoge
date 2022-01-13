<template>
    <header>
        <div class="navbar">
            <img src="@/assets/images/logo.png" class="logo">
            <div class="nav-toggle">
                <img src="@/assets/icons/close.svg" class="close"
                    @click="closeDropdown" v-if="showingDropdown">
                <img src="@/assets/icons/hamburger.svg" class="hamburger"
                    @click="openDropdown" v-if="!showingDropdown">
            </div>
        </div>

        <NavLinks class="dropdown" />
    </header>
</template>

<script>
import NavLinks from './NavLinks.vue'
import gsap from 'gsap'
import { ref } from '@vue/reactivity'
import { onMounted } from '@vue/runtime-core'

export default {
    components: { NavLinks },
    setup() {
        const showingDropdown = ref(false)

        const openDropdown = () => {
            animateDropdown.play()
            showingDropdown.value = true
        }
        const closeDropdown = () => {
            animateDropdown.reverse()
            showingDropdown.value = false
        }

        let animateDropdown

        onMounted(() => {
            gsap.set('.dropdown', {scaleY:0})
            gsap.set('.dropdown li', {opacity:0, scale:0.2})
            animateDropdown = gsap.timeline({paused:true, defaults:{duration:0.4}})
                .to('.dropdown', {scaleY:1, ease:'back'})
                .to('.dropdown li', {scale:1, opacity:1}, '-=0.1')
        })

        return { showingDropdown, openDropdown, closeDropdown }

    }
}
</script>

<style>
header {
    padding: 0 10px;
    background: var(--primary);
    position: sticky;
    position: -webkit-sticky;
    top: 0;
    box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.25);
}
.navbar {
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
}
.logo {
    width: 220px;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
}
.nav-toggle {
    height: 44px;
}
.hamburger, .close {
    cursor: pointer;
    width: 44px;
}
.nav-links {
    padding: 10px 0 24px;
}
nav.dropdown {
    background: var(--primary);
    box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.25);
    transform-origin: top;
    position: absolute;
    width: 100%;
    left: 0;
}
nav li {
    padding: 12px 0;
}
nav a {
    color: var(--lambdoge);
    text-decoration: none;
}
nav a:hover {
    color: white;
}
</style>