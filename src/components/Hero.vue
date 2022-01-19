<template>
    <section id="hero">
        <img src="@/assets/images/hero.svg" class="lambdoge-hero" alt="lambdoge hero">
        <h2>Comic Books For <br> Us, By Us</h2>
        <p>A comic book series that is written by, voted on and enjoyed by the LambDoge community.</p>
        <div class="buttons">
            <a href="https://opensea.io/lambdoge" target="_blank" class="button btn-solid">
                Read Comics
            </a>
            <a href="https://rocketswap.exchange/#/swap/con_lambdoge" target="_blank" class="button btn-outline">
                Buy $LDOGE
            </a>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style>
.lambdoge-hero {
    width: 100%;
    max-width: 400px;
}
#hero h2 {
    color: var(--secondary);
    margin: 10px 0 5px;
}
#hero p {
    max-width: 340px;
    margin: 0 auto;
}
@media screen and (min-width: 680px) {
    .lambdoge-hero {
        max-width: 440px;
    }
    #hero p {
        max-width: 420px;
    }
    #hero .buttons {
        display: flex;
        max-width: 500px;
        margin: 10px auto;
    }
    #hero .button {
        margin: 15px 10px;
    }
    #hero br {
        display: none;
    }
}
@media screen and (min-width: 960px) {
    .lambdoge-hero {
        max-width: 550px;
    }
    #hero p {
        max-width: 500px;
    }
}
@media screen and (min-width: 1200px) {
    .lambdoge-hero {
        max-width: 670px;
    }
}
</style>