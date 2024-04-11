<template>
    <div class="sales-analytics">

        <div class="shop-card">
            <div class="left">
                <div class="card-title">
                    <diV class="card-content">
                        <img src="~assets/images/logo_light.svg" />
                        <h3>Shop Point</h3>
                    </diV>
                </div>
                <div class="card-retail">
                    <div class="retail-title">
                        <h3>ShopPoint - Retail</h3>
                        <div class="retail-description">
                            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Cum, ullam.</p>
                        </div>
                    </div>

                    <div class="retail-time">
                        <div class="time">Average Rate 2023</div>
                        <!-- <i class="retail-link">i</i> -->
                    </div>

                    <div class="retail-content">
                        <div class="retail-service">
                            <div class="retail-order">
                                <div class="retail-img green">
                                    <i class="el-icon-coin"></i>
                                </div>
                                <div class="retail-price">
                                    <h2>$15,412</h2>
                                    <p>income</p>
                                    <p class="price">+45.21%</p>
                                </div>
                            </div>
                        </div>
                        <div class="retail-service">
                            <div class="retail-order">
                                <div class="retail-img pink ">
                                    <i class="el-icon-sell"></i>
                                </div>
                                <div class="retail-price">
                                    <h2>$5,318</h2>
                                    <p>income</p>
                                    <p class="price red">+45.21%</p>
                                </div>
                            </div>
                        </div>
                        <div class="retail-service">
                            <div class="retail-order">
                                <div class="retail-img blue">
                                    <i class="el-icon-shopping-bag-2"></i>
                                </div>
                                <div class="retail-price">
                                    <h2>$5,412</h2>
                                    <p>income</p>
                                    <p class="price">+45.21%</p>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
                <div class="card-price"></div>
            </div>
            <div class="right">
                <div class="card-content">
                    <div class="card-img">
                        <img src="~assets/images/login.webp" width="70px" />
                    </div>
                    <div class="card-price">
                        <div class="card-money">$476,3k</div>
                        <div class="card-total">Total Balance</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="revenue">
            <div class="apexchart">
                <div class="apexchart-card">
                    <client-only>
                        <apex-chart type="bar" height="350" :options="data.chartOptions"
                            :series="data.series"></apex-chart>
                    </client-only>
                </div>
            </div>
            <div class="chart">
                <div class="chart-card">
                    <div class="chart-title">Total Report</div>
                    <div class="chart-text">
                        <p>
                            All Periods per 01/01/2022 - 08/28/2023
                        </p>
                    </div>
                    <div class="chart-revenue">
                        <div>Revenue</div>
                        <div>$176,120</div>
                        <div>+45%</div>
                    </div>
                    <div class="chart-revenue">
                        <div>Revenue</div>
                        <div>$176,120</div>
                        <div>+45%</div>
                    </div>
                    <div class="chart-revenue">
                        <div>Revenue</div>
                        <div>$176,120</div>
                        <div>+45%</div>
                    </div>

                </div>
                <div class="btn-detail">
                    <button class="detail">More Details</button>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent, reactive, toRefs, } from '@nuxtjs/composition-api'



export default defineComponent({

    setup() {

        const state = reactive({
            data: {

                series: [{
                    name: 'Net Profit',
                    data: [44, 55, 57, 56, 61, 58, 63, 60, 66]
                }, {
                    name: 'Revenue',
                    data: [76, 85, 101, 98, 87, 105, 91, 114, 94]
                }, {
                    name: 'Free Cash Flow',
                    data: [35, 41, 36, 26, 45, 48, 52, 53, 41]
                }],
                chartOptions: {
                    chart: {
                        type: 'bar',
                        height: 350
                    },
                    plotOptions: {
                        bar: {
                            horizontal: false,
                            columnWidth: '55%',
                            endingShape: 'rounded'
                        },
                    },
                    dataLabels: {
                        enabled: false
                    },
                    stroke: {
                        show: true,
                        width: 2,
                        colors: ['transparent']
                    },
                    xaxis: {
                        categories: ['Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct'],
                    },
                    yaxis: {
                        title: {
                            text: '$ (thousands)'
                        }
                    },
                    fill: {
                        opacity: 1
                    },
                    tooltip: {
                        y: {
                            formatter: function (val) {
                                return "$ " + val + " thousands"
                            }
                        }
                    }
                },


            },
        })
        return { ...toRefs(state), };
    }
})
</script>

<style lang="scss">
@media screen and (max-width: 1285.60px) {
    .shop-card {
        .left {
            width: 100% !important;

        }

        .right {
            display: none;
        }

    }

}



.sales-analytics {

    padding: 10px 30px;



    .shop-card {
        margin-top: 30px;
        gap: 20px;
        padding: 10p 20px;
        width: 100%;
        display: flex;
        align-items: center;

        .left {
            display: flex;
            width: 60%;
            background: #FFFFFF;

            .card-title {

                padding: 30px;

                .card-content {
                    display: flex;
                    align-items: center;
                    flex-direction: column;
                    gap: 20px;
                    background: #F9F9F9;
                    border: 1px solid rgba(0, 0, 0, 0.2);
                    border-radius: 5px;
                    padding: 40px 40px;

                    h3 {
                        font-size: 17px;
                        font-weight: bold;
                    }
                }

                img {
                    width: 90px;
                    height: 90px;
                }
            }

            .card-retail {
                padding: 20px 20px;
                width: 100%;

                h3 {
                    font-size: 25px;
                    font-weight: bold
                }

                .retail-content {
                    display: flex;
                    justify-content: space-between;
                    gap: 20px;
                    width: 100%
                }

                .retail-time {
                    display: flex;
                    gap: 20px;

                    .time {
                        font-size: 20px;
                        font-weight: bold;
                    }
                }

                .retail-service {
                    .retail-order {
                        padding: 20px 0;
                        display: flex;
                        gap: 10px;

                        .retail-img {
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            margin-top: 10px;
                            border-radius: 5px;
                            padding: 20px;
                            width: 50px;
                            height: 47px;
                            background: green;
                            color: white;

                            i {
                                font-size: 17px;
                            }
                        }

                        .pink {
                            background: rgb(222, 12, 166);

                        }

                        .blue {
                            background: blue;
                        }

                        .retail-price {
                            .price {
                                color: green
                            }

                            .red {
                                color: red;
                            }

                        }
                    }
                }
            }
        }

        .right {
            background: linear-gradient(to right, rgb(202, 234, 242), rgb(183, 238, 245), rgb(32, 161, 225), rgb(7, 181, 239), );
            width: 40%;
            padding: 20px;

            .card-content {
                display: flex;
                align-items: center;
                width: 100%;
                height: 275px;

                .card-img {
                    width: 300px;

                    img {
                        width: 250px;

                    }
                }

                .card-price {
                    .card-money {
                        font-size: 35px;
                        font-weight: bold;
                        color: #000;
                    }

                    .card-total {
                        font-size: 20px;
                        color: #000;
                        font-weight: 600;
                    }
                }
            }
        }

    }

    .revenue {
        display: flex;
        gap: 20px;
        margin-top: 20px;

        .apexchart {
            width: 60%;
            background: #FFFFFF;
        }

        .chart {
            width: 40%;
            background: #FFFFFF;

            .chart-card {
                padding: 20px 40px;

                .chart-title {
                    font-size: 25px;
                    color: #000;
                    font-weight: bold;
                }

                .chart-text {
                    p {
                        color: rgb(165, 153, 153);
                        font-weight: 600;
                    }

                }

                .chart-revenue {
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    background: #F9F9F9;
                    padding: 20px 40px;
                    margin-top: 20px;

                }
            }

            .btn-detail {
                padding: 20px 40px;
                width: 100%;

                .detail {
                    border: #01C8A9;
                    box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
                    width: 100%;
                    color: #fff;
                    font-size: 17px;
                    font-weight: bold;
                    background: #00BA9D;
                    border-radius: 23px;
                    padding: 10px 0;
                }
            }
        }
    }


}
</style>