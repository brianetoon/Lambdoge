<template>
    <div class="token-info">
        <h3>More Info</h3>
        <ul>
            <li v-for="(item, i) in items" :key="i">
                <a :href="item.href" target="_blank">{{ item.link }}</a>
                <span class="note">{{ item.note }}</span>
            </li>
        </ul>
    </div>
</template>

<script>
import store from '@/store.js'
import { ref } from '@vue/reactivity'

export default {
    setup() {
        const items = ref(store.tokenomics)

        return { items }
    }
}
</script>

<style>
.token-info {
    max-width: 400px;
    margin: 80px auto 20px;
    padding: 30px 30px 30px 45px;
    border: 2px solid white;
    border-radius: 8px;
}
.token-info h3 {
    color: white;
    text-align: left;
    margin-bottom: 12px;
}
.token-info ul {
    list-style-type: disc;
    color: var(--primary);
}
.token-info li {
    text-align: left;
    font-size: 16px;
    font-weight: 500;
    line-height: 28px;
}
.token-info li a {
    color: var(--primary);
    text-decoration: underline;
}
.token-info li a:hover {
    color: var(--secondary);
}
.note {
    color: white;
}

@media screen and (min-width: 680px) {
    .token-info {
        max-width: 500px;
    }
    .token-info li {
        font-size: 17px;
        margin-bottom: 2px;
    }
}
@media screen and (min-width: 960px) {
    .token-info {
        max-width: 900px;
        padding: 30px 30px 50px 50px;
    }
}
</style>