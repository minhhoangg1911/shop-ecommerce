<template>
    <div class="seller-table">
        <ViewPageProfile />
        <div class="table">
            <el-table :data="state.tableData" style="width: 100%">
                <el-table-column prop="seller" label="Seller" width="180">
                    <div class="table-seeler">
                        <img src='~assets/images/google.png' />
                        <address>
                            <div>
                                <nuxt-link class="link" to="">www.website.com</nuxt-link>
                            </div>
                            <div>
                                <nuxt-link to="">+1(135) 744-8315</nuxt-link>
                            </div>
                            <div> <nuxt-link to="">email@gmail.com</nuxt-link></div>
                        </address>
                    </div>
                </el-table-column>

                <el-table-column prop="order" label="Orders Value" width="180">
                    <div class="table-order">
                        <h1>65,874</h1>
                        <span>New orders</span>
                        <div>
                            <i class="el-icon-caret-top"></i>
                            <span>+55,96%</span>
                        </div>
                    </div>
                </el-table-column>
                <el-table-column prop="income" label="Income Value">
                    <div class="table-income">
                        <h1>$23k</h1>
                        <span>Income</span>
                        <div>
                            <i class="el-icon-caret-top"></i>
                            <span>+14,56%</span>
                        </div>
                    </div>
                </el-table-column>
                <el-table-column prop="review" label="Review Rate">
                    <div>
                        <el-rate v-model="state.rate" disabled show-score text-color="#ff9900"
                            score-template="{value} points">
                        </el-rate>
                    </div>
                </el-table-column>
                <el-table-column prop="sale" label="Sales Categories Value">
                    <div class="table-sale">
                        <div class="table-service">
                            <div>Electronucs</div>
                            <div>
                                <span>$10.55k</span>
                            </div>
                        </div>
                        <div class="table-service">
                            <div>Fashion</div>
                            <div>
                                <span>$40.88k</span>
                            </div>
                        </div>
                        <div class="table-service">
                            <div>Food & Drinks</div>
                            <div>
                                <span>$36.95k</span>
                            </div>
                        </div>
                        <div class="table-service">
                            <div>Services</div>
                            <div>
                                <span>$487</span>
                            </div>
                        </div>

                    </div>
                </el-table-column>
                <el-table-column class="table-container" prop="other" label="Other">
                    <div class="table-other">
                        <i class="el-icon-edit-outline"></i>
                        <i class="el-icon-more rotate"></i>
                    </div>
                </el-table-column>

            </el-table>
            <div class="pagination" >
                <el-pagination background layout="prev, pager, next" :total="40">
                </el-pagination>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent, reactive } from '@nuxtjs/composition-api'
import ViewPageProfile from '~/components/ViewProfile/ViewPageProfile.vue'
export default defineComponent({
    components: {
        ViewPageProfile,
    },
    setup() {
        const state = reactive({
            rate: 5,
            tableData: [
                {
                    seller: '2016-05-03',
                    order: 'Tom',
                    income: 'No. 189, Grove St, Los Angeles',
                    review: '123',
                    sale: "568",
                    other: "321",
                },
                {
                    seller: '2016-05-03',
                    order: 'Tom',
                    income: 'No. 189, Grove St, Los Angeles',
                    review: '123',
                    sale: "100%",
                    other: "321",
                },
                {
                    seller: '2016-05-03',
                    order: 'Tom',
                    income: 'No. 189, Grove St, Los Angeles',
                    review: '123',
                    sale: "100%",
                    other: "321",
                },


            ],
        })
        return { state }
    },
})
</script>

<style lang="scss">
.seller-table {
    padding: 0 30px;

    .table {
        margin: 20px 0;

        .el-rate__icon {
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 25px;
        }

        .el-rate__text {
            display: none;
        }

        .el-table__header-wrapper {
            padding: 20px;

            .cell {
                color: #035ECF;
                font-size: 15px;
                font-weight: bold;

            }
        }

        .el-table__cell {
            padding: 0 20px;
        }
    }

    .table-seeler {

        padding: 20px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;

        img {
            max-width: 50px;
            padding: 10px;
            border: 1px solid rgba(0, 0, 0, 0.2);
        }

        address {
            div {
                a {
                    padding: 20px 0;
                }

                .link {
                    color: blue;
                    font-size: 13px;

                }

                ;
            }

        }
    }

    .table-order {
        padding: 20px;

        span {
            font-size: 14px;
            font-weight: 700;
            color: #6E757F;
            font-family: "Archivo SemiExpanded", sans-serif;

        }

        h1 {
            font-size: 23px;
            font-weight: bold;
        }

        div {
            display: flex;
            align-items: center;
            color: green;
            font-size: 15px;
            font-weight: bold;

            i {
                font-size: 20px;
            }
        }
    }

    .table-income {
        padding: 20px;

        span {
            font-size: 14px;
            font-weight: 700;
            color: #6E757F;
            font-family: "Archivo SemiExpanded", sans-serif;

        }


        h1 {
            font-size: 23px;
            font-weight: bold;
        }

        div {
            display: flex;
            align-items: center;
            color: green;
            font-size: 15px;
            font-weight: bold;

            span {
                color: green;
            }

            i {
                font-size: 20px;
            }
        }

    }

    .table-sale {
        .table-service {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 15px;
            padding: 5px 0;
            font-weight: 700;
            color: #6E757F;
            font-family: "Archivo SemiExpanded", sans-serif;

            div {
                span {
                    color: black;

                }
            }
        }
    }

    .el-table_1_column_6 {
        text-align: center;
    }

    .table-other {
        text-align: center;
        padding: 0 20px;
        margin-left: 20px;

        i {
            font-size: 25px;
            color: #035ECF;
        }

        .rotate {
            transform: rotate(90deg);
            display: inline-block;
        }
    }

    .pagination {
        margin-top: 20px;
        .el-pagination {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    }
   


}
</style>
