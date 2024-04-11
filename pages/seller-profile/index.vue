<template>
    <div class="example">
       
        <client-only>
            <apex-chart type="line" height="500" width="100%" :options="chartOptions" :series="series"></apex-chart>
        </client-only>

    </div>
</template>

<script>
import { defineComponent, reactive, toRefs, } from '@nuxtjs/composition-api'
import dayjs from 'dayjs'



export default defineComponent({
   
    setup() {

        const state = reactive({
            chartOptions: {
                chart: {
                    id: 'basic-bar'
                },
                xaxis: {
                    categories: [dayjs(new Date()).format('DD MMMM')]
                }
            },
            series: [{
                name: 'series-1',
                data: ['0$', '3$', '1$', '1$', '4$',]
            }]
        })
        return { ...toRefs(state), };
    }


})
</script>
