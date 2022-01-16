<template>
    <div class="desktop-nav">
        <div class="nav-content">
            <img src="@/assets/images/logo.png" class="logo">
            <NavLinks :offset="100" />
            <div class="icon-buttons">
                <a href="https://t.me/lambdoge" target="_blank">
                    <img src="@/assets/icons/telegram_yellow.svg" class="icon">
                </a>
                <a href="https://twitter.com/lambdoge" target="_blank">
                    <img src="@/assets/icons/twitter_yellow.svg" class="icon">
                </a>
            </div>
        </div>
    </div>
</template>

<script>
import NavLinks from './NavLinks.vue'

export default {
    components: { NavLinks }
}
</script>

<style>
.desktop-nav .nav-content {
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.desktop-nav .logo {
    width: 220px;
}
.desktop-nav .nav-links {
    display: flex;
}
.desktop-nav li {
    margin: 0 18px;
}
.desktop-nav .icon:not(first-child) {
    margin-left: 16px;
}
</style>