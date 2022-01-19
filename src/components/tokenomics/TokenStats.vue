<template>
    <div class="token-stats">
        <p class="founders">7.5% Founders Wallet <br> 75,000,000,000 (75 billion)</p>
        <p class="farms">12.5% Farms Distribution <br> 121,500,000,000 (121.5 billion)</p>
        <p class="rocket">1.35% RSWP - LDOGE <br> 13,500,000,000 (13.5 billion)</p>
        <p class="developers">5% Developers Wallet <br> 50,000,000,000 (50 billion)</p>
        <p class="advisors">1.5% Advisors <br> 15,000,000,000 (15 billion)</p>
        <p class="liquidity">72.5% Liquidity <br> 725,000,000,000 (725 billion)</p>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.token-stats p {
    margin-bottom: 22px;
}
.founders {
    color: #99EBBD;
}
.farms {
    color: var(--primary);
}
.rocket {
    color: var(--secondary);
}
.developers {
    color: var(--lambdoge);
}
.advisors {
    color: #FCDDEC;
}
.liquidity {
    color: #A26BFA;
}

@media screen and (min-width: 960px) {
    .token-stats p {
        position: absolute;
    }
    .founders {
        top: 0px;
        left: 200px;
    }
    .farms {
        top: 70px;
        left: 90px;
    }
    .rocket {
        top: 140px;
        left: 65px;
    }
    .developers {
        top: 210px;
        left: 65px
    }
    .advisors {
        top: 280px;
        left: 100px;
    }
    .liquidity {
        right: 50px;
        top: 50%;
        transform: translateY(-50%)
    }
}
</style>