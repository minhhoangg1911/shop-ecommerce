<template>
    <div class="seller-content">
        <div class="seller-view">
            <h4>Sales period:</h4>
            <p>View profiles: 4/12</p>
        </div>
        <div class="seller-date">
            <div class="block">
                <el-date-picker v-model="values" type="daterange" start-placeholder="Start date"
                    end-placeholder="End date" :default-time="['00:00:00', '23:59:59']">
                </el-date-picker>
            </div>
            <div class="select">
                <el-select v-model="state.value" placeholder="Best Selling">
                    <el-option v-for="item in state.options" :key="item.value" :label="item.label" :value="item.value">
                    </el-option>
                </el-select>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent,ref,reactive } from '@nuxtjs/composition-api'

export default defineComponent({
    setup() {
        const values = ref('')

        const state = reactive({
            rate: 3.7,
            options: [
                {
                    value: 'Option1',
                    label: 'Best Selling',
                },
                {
                    value: 'Option2',
                    label: 'Rating: High to Low',
                },
                {
                    value: 'Option3',
                    label: 'Rating: Low to High',
                },
                {
                    value: 'Option4',
                    label: 'By name: A-Z',
                },
                {
                    value: 'Option5',
                    label: 'By name: Z-A',
                },
            ],
            value: '',
        })

        return { values, state }
    },
})
</script>

<style lang="scss">
    .seller-content {
        .seller-view {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .seller-date {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
    }
</style>