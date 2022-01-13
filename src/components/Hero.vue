<template>
    <section id="hero">
        <img src="@/assets/images/hero.svg" class="hero" alt="lambdoge hero">
        <h2>Comic Books For <br> Us, By Us</h2>
        <p>A comic book series that is written by, voted on and enjoyed by the LambDoge community.</p>
        <button class="btn-solid">Read Comics</button>
        <button class="btn-outline">Buy $LDOGE</button>
    </section>
</template>

<script>
export default {

}
</script>

<style>
#hero h2 {
    color: var(--secondary);
}
.hero {
    width: 100%;
    max-width: 400px;
}
</style>