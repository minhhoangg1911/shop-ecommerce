<template>
    <div class="page-sale-period">

        <div class="seller-view">
            <h4>Sales period:</h4>
            <p>Popular Tags:</p>
        </div>
        <div class="seller-date">
            <div class="block">
                <el-date-picker v-model="values" type="daterange" start-placeholder="Start date"
                    end-placeholder="End date" :default-time="['00:00:00', '23:59:59']">
                </el-date-picker>
            </div>
            <div class="select">
                <div>
                    <button>Top Rated</button>
                </div>
                <div>
                    <button>New In</button>
                </div>
                <div>
                    <button>Best Sellers</button>
                </div>
                <div>
                    <button>A-Z </button>
                </div>
                <div>
                    <button>Reviews</button>
                </div>

            </div>
        </div>

    </div>
</template>


<script>
import { defineComponent, ref,} from '@nuxtjs/composition-api'

export default defineComponent({
    setup() {
        const values = ref('')
        return { values,  }
    },
})
</script>

<style lang="scss">
.page-sale-period {
    .seller-view {
        display: flex;
        justify-content: space-between;
        align-items: center;
        p{
            font-size: 20px;
            font-weight: bold;
            
        }
    }

    .seller-date {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .select {
        display: flex;
        gap: 10px;
        button {
            border-radius: 30px;
            border: 1px solid #035ECF;
            padding: 5px 15px;
            font-size: 15px;
            font-weight: bold;
            color: #035ECF;
            transition: ease-in-out 0.5s;
            &:hover {
                background: blue;
                color: #ffffff;
                transition: ease-in-out 0.5s;
            }
        }
    }
}
</style>