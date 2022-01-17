<template>
    <footer>
        <div class="footer">
            <img src="@/assets/images/logo.png" class="logo">
            <p class="copyright">&copy; 2022 LambDoge</p>
            <div class="icon-buttons">
                <a href="https://t.me/lambdoge" target="_blank">
                    <img src="@/assets/icons/telegram_blue.svg" class="icon">
                </a>
                <a href="https://twitter.com/lambdoge" target="_blank">
                    <img src="@/assets/icons/twitter_blue.svg" class="icon">
                </a>    
            </div>
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style>
footer {
    padding: 85px 0;
}
footer .logo {
    width: 90%;
    max-width: 330px;
}
.copyright {
    margin: 20px 0 30px;
}
footer .icon {
    margin: 0 12px;
}
</style>