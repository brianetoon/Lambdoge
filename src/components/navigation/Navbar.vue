<template>
    <header>
        <MobileNav />
        <DesktopNav />
    </header>
</template>

<script>
import MobileNav from './MobileNav.vue'
import DesktopNav from './DesktopNav.vue'
export default {
    components: { MobileNav, DesktopNav }
}
</script>

<style>
header {
    padding: 0 20px;
    background: var(--primary);
    position: sticky;
    position: -webkit-sticky;
    top: 0;
    box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.25);
}
.desktop-nav {
    display: none;
}
nav a {
    color: var(--lambdoge);
    text-decoration: none;
    cursor: pointer;
    font-weight: 500;
}
nav a:hover {
    color: white;
}

@media screen and (min-width: 960px) {
    .mobile-nav {
        display: none;
    }
    .desktop-nav {
        display: block;
    }
    header {
        margin: 10px;
        top: 10px;
        border-radius: 6px;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.1);
    }
    nav a {
        font-weight: 700;
    }
}
@media screen and (min-width: 1300px) {
    header {
        max-width: 1280px;
        margin: 10px auto;
    }
}
</style>