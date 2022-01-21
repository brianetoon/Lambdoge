<template>
    <section id="mission">
        <h2>Our Mission</h2>
        <div class="text">
            <p><strong>LambDoge is a decentralized comic book series</strong> that is entirely and voted on by the community to decide on the direction of the storyline. All comics will be drawn by professional artists and then minted as NFTs.</p>
            <p>This comic can and will go anywhere our minds can take us. Strap in because it's going to be a wild ride!</p>
        </div>
        <div class="comics grid">
            <img :src="require(`@/assets/images/${comic}`)"
                v-for="(comic, i) in comics" :key="i" class="grid-item">
        </div>
        <div class="buttons">
            <a href="https://opensea.io/lambdoge" target="_blank" class="button btn-solid">
                Read Comics
            </a>
            <a href="https://t.me/lambdoge" target="_blank" class="button btn-outline btn-icon">
                <img src="@/assets/icons/telegram_red.svg" class="icon-in-btn">
                Join the fun on Telegram
            </a>
        </div>
    </section>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup() {
        const comics = ref(['comic_1.svg', 'comic_2.svg', 'comic_3.svg'])

        return { comics }
    }
}
</script>

<style>
#mission {
    max-width: 420px;
}
.comics img {
    width: 100%;
}
.text p { 
    margin: 10px auto;
}

@media screen and (min-width: 680px) {
    #mission {
        max-width: 100%;
    }
    .text p {
        max-width: 100%;
    }
}

@media screen and (min-width: 960px) {
    #mission .buttons {
        display: flex;
        justify-content: center;
    }
    #mission .button {
        margin: 10px 15px;
    }
}
</style>
