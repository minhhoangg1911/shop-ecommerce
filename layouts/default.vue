<template>
    <div>
        <page-header />
        <nuxt />
        <page-footer />
    </div>
</template>


<script>
import { defineComponent } from '@nuxtjs/composition-api'
import PageHeader from '@/components/Header/PageHeader'
import PageFooter from '@/components/Footer/PageFooter'
export default defineComponent({
    components: {
        PageHeader,
        PageFooter
    },
    setup() {
        
    },
})
</script>


<style lang="scss">

</style>