<template>
    <div class="figure">
        <img src="@/assets/images/circle_graph.svg" class="donut">
        <p class="supply">Total Supply <br> 1,000,000,000,000 <br> (1 trillion)</p>
        <TokenStats class="desktop-stats" />
    </div>
    <TokenStats class="mobile-stats" />
</template>

<script>
import TokenStats from './TokenStats.vue'
export default {
    components: { TokenStats }
}
</script>

<style>
.figure {
    position: relative;
    margin: 20px auto;
}
.donut {
    max-width: 325px;
}
.desktop-stats {
    display: none;
}
.supply {
    color: white;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}
@media screen and (min-width: 680px) {
    .donut {
        max-width: 350px;
    }
}

@media screen and (min-width: 960px) {
    .figure {
        max-width: 960px;
        margin-top: 60px;
    }
    .desktop-stats {
        display: block;
    }
    .mobile-stats {
        display: none;
    }
    .donut {
        margin: 50px 0;
    }
}
</style>