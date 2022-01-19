<template>
    <section id="tokenomics">
        <h2>Tokenomics</h2>
        <TokenFigure />
        <a href="https://rocketswap.exchange/#/swap/con_lambdoge" target="_blank" class="button btn-solid">
            Buy $LDOGE
        </a>
        <TokenInfo />
    </section>
</template>

<script>
import TokenFigure from './TokenFigure.vue'
import TokenInfo from './TokenInfo.vue'

export default {
    components: { TokenFigure, TokenInfo }
}
</script>

<style>
#tokenomics {
    padding: 80px 25px;
    background: #221E22;
    margin-bottom: 0;
}
#tokenomics h2 {
    text-shadow: none;
    color: white;
}
#tokenomics .button {
    margin-top: 60px;
}

@media screen and (min-width: 680px) {
    #tokenomics {
        padding: 100px 30px
    }
    #tokenomics p {
        font-size: 17px;
    }
}
@media screen and (min-width: 960px) {
    #tokenomics {
        padding: 100px 0;
    }
    #tokenomics .button {
        margin-top: 0;
    }
}
</style>