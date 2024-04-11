<template>
    <div>
        <page-header />
        <page-sellers />
        <nuxt />
        <page-footer />
    </div>
</template>


<script>
import { defineComponent } from '@nuxtjs/composition-api'
import PageHeader from '@/components/Header/PageHeader'
import PageSellers from '~/components/SellerComponent/PageSellers.vue'
import PageFooter from '@/components/Footer/PageFooter'

export default defineComponent({
    components: {
        PageHeader,
        PageFooter,
        PageSellers,
    },
    setup() {
        
    },
})
</script>


<style lang="scss">
    body {
        background: #F9F9F9;
    }
</style>