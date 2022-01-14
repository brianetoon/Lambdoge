<template>
    <footer>
        <div class="footer">
            <img src="@/assets/images/logo.png" class="logo">
            <p class="copyright">&copy; 2022 LambDoge</p>
            <div class="icon-buttons">
                <img src="@/assets/icons/telegram_blue.svg" class="icon">
                <img src="@/assets/icons/telegram_blue.svg" class="icon">
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
    width: 42px;
    margin: 0 12px;
    cursor: pointer;
}
</style>