<template>
    <div class="seller-grid">
        <ViewPageProfile />
        <div class="grid">
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>
            <div class=grid-item>
                <div>
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div>
                    <i class="el-icon-more"></i>
                </div>
            </div>

        </div>
        <div class="pagination">
            <el-pagination background layout="prev, pager, next" :total="20">
            </el-pagination>
        </div>
    </div>
</template>

<script>
import { defineComponent } from '@nuxtjs/composition-api'
import ViewPageProfile from '~/components/ViewProfile/ViewPageProfile.vue';


export default defineComponent({
    components: { ViewPageProfile },
    conponents: {
        ViewPageProfile,
    },
    setup() {

    }
})
</script>
<style lang="scss">
.seller-grid {
    padding: 0 30px;

    .grid {
        display: grid;
        grid-template-columns: repeat(6, minmax(0, 1fr));
        gap: 20px;

        margin-top: 25px;

        .grid-item {
            background: #ffffff;
            padding: 20px 40px;
            display: flex;
            border-radius: 5px;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);

            i {
                transform: rotate(90deg);
                font-size: 30px;
                color: #035ECF;
            }
        }
    }

    .pagination {
        margin-top: 20px;
    }
}

@media screen and (max-width: 1285.60px) {
    .grid {
        grid-template-columns: repeat(5, minmax(0, 1fr)) !important;
    }
}

@media screen and (max-width: 1270.60px) {
    .grid {
        grid-template-columns: repeat(3, minmax(0, 1fr)) !important;
    }
}

@media screen and (max-width: 760.60px) {
    .grid {
        grid-template-columns: repeat(2, minmax(0, 1fr)) !important;
    }
}

@media screen and (max-width: 620.60px) {
    .grid {
        grid-template-columns: repeat(1, minmax(0, 1fr)) !important;
    }
}
</style>