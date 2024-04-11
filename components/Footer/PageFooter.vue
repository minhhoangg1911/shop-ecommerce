<template>
    <div class="footer">
        <div class="footer-text">
            <p>Copyright @ 2024 By Merkulove All Right Reserved</p>
        </div>
        <div class="footer-img">
            <div>
                <span>Powered by</span>
            </div>
            <img src="~assets/images/footer/merkulove.png" />
        </div>
    </div>
</template>

<script>
import { defineComponent } from '@nuxtjs/composition-api'



export default defineComponent({
    setup() {


    }

})
</script>

<style lang="scss">
.footer {
    padding: 20px 30px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .footer-text {
        p {
            font-size: 12px;
            display: inline;
        }
    }
    .footer-img {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;
        span {
            font-size: 12px;
        }
    }
}
</style>