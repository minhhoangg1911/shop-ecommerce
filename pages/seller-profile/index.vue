<template>
    <div class="seller-profile">
        <sale-period />
        <div class="seller-card">

            <div class="card-link">
                <div class="card-img">
                    <img src="~assets/images/seller-grid/4.webp" />
                </div>
                <div class="card-name">
                    <h1>Delight</h1>
                    <address>
                        <div>
                            <nuxt-link class="link" to="">www.website.com</nuxt-link>
                        </div>
                        <div>
                            <nuxt-link to="">1+(328) 765-3065</nuxt-link>
                        </div>
                        <div>
                            <nuxt-link to="">email@gmail.com</nuxt-link>
                        </div>
                    </address>
                </div>

            </div>


            <div class="card-price">
                <div class="card-service">
                    <i class="el-icon-d-arrow-right icon"></i>
                    <p>Transactions</p>
                    <div class="card-revenu">
                        <i class="el-icon-caret-top"></i>
                        <span class="">+14,56%</span>
                    </div>
                    <h1>$96k</h1>
                </div>
                <div>
                    <i class="el-icon-more rotate"></i>
                </div>

            </div>

            <div class="card-chart">
                <div class="card-title">Sale Activity</div>
                <client-only>
                    <apex-chart type="bar" height="350" :options="chartOne.data.chartOptions"
                        :series="chartOne.data.series"></apex-chart>
                </client-only>
            </div>


            <div class="card-description">
                <div class="card-detail">
                    <img src="~assets/images/seller-profile/credit-card.webp" />
                    <h1>Total Expense</h1>
                    <span>$32.1k</span>
                </div>
                <div class="card-detail">
                    <img src="~assets/images/seller-profile/wallet.webp" />
                    <h1>Total Profit</h1>
                    <span>$144.1k</span>
                </div>
            </div>
        </div>

        <div class="seller-chart">
            <div class="chart-rating">
                <div class="chart">
                    <client-only>
                        <apex-chart type="line" height="500" width="100%" :options="chartOptions"
                            :series="series"></apex-chart>
                    </client-only>
                </div>
                <div class="seller-rating">
                    <div class="rating-content">
                        <div class="rating-content-title">Sales Profit by Category:</div>
                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Electronics</div>
                                    <span>$6.34k</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="26" :percentage="30"></el-progress>
                            </div>
                        </div>

                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Fashion</div>
                                    <span>$2.52k</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="24" :percentage="20"
                                    status="success"></el-progress>
                            </div>
                        </div>
                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Food & Drinks</div>
                                    <span>$12.10k</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="22" :percentage="50"
                                    status="warning"></el-progress>
                            </div>
                        </div>
                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Services</div>
                                    <span>$5.00k</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="20" :percentage="25"
                                    status="exception"></el-progress>
                            </div>
                        </div>


                        <div class="review-title">
                            <h1>Review Rate</h1>
                            <div>From 324 Responders</div>
                        </div>
                        <div class="review-rate">
                            <div>
                                <el-rate v-model="value" disabled show-score text-color="#ff9900"
                                    score-template="{value}">
                                </el-rate>
                            </div>
                            <div class="review-detail">View All Review</div>
                        </div>

                    </div>


                    <div class="service">
                        <div class="service-card">
                            <i class="el-icon-bank-card blue"></i>
                            <div>
                                <h3>$23.4k</h3>
                                <span>Income</span>
                            </div>
                        </div>
                        <div class="service-card">
                            <i class="el-icon-camera-solid green"></i>
                            <div>
                                <h3>234</h3>
                                <span>New Orders</span>
                            </div>
                        </div>
                        <div class="service-card">
                            <i class="el-icon-news pink"></i>
                            <div>
                                <h3>$123</h3>
                                <span>Expense</span>
                            </div>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent, reactive, toRefs, } from '@nuxtjs/composition-api'
import dayjs from 'dayjs'
import SalePeriod from '~/components/SalePeriod/SalePeriod'

export default defineComponent({

    conponents: {
        SalePeriod
    },
    setup() {

        const state = reactive({
            chartOne: {
                data: {

                    series: [{
                        name: 'Net Profit',
                        data: [1, 1, 1, 1, 1, 1, 3]
                    }, {
                        name: 'Revenue',
                        data: [11, 1, 1, 1, 1, 1, 1]
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

            },

            value: 3.7,
            chartOptions: {
                chart: {
                    id: 'basic-bar'
                },
                xaxis: {
                    categories: [dayjs(new Date()).format('DD MMMM'), dayjs(new Date(2024, 3, 14)).format('DD MMMM'), dayjs(new Date(2024, 3, 16)).format('DD MMMM'), dayjs(new Date(2024, 3, 18)).format('DD MMMM'), dayjs(new Date(2024, 3, 20)).format('DD MMMM'),]
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
<style lang="scss">
.seller-profile {
    padding: 0 30px;

    .seller-card {
        padding: 20px 0;
        display: flex;
        gap: 30px;

        .card-link {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            background: #ffffff;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
            padding: 20px;

            .card-img {
                padding: 20px;
                border: 1px solid rgba(0, 0, 0, 0.1);
                border-radius: 5px;

                img {
                    width: 120px;

                }
            }

            .card-name {
                display: flex;
                flex-direction: column;
                padding: 0 30px;

                .link {
                    color: #035ECF;
                    font-weight: 700;
                    line-height: 1.1;
                }

                h1 {
                    font-size: 27px;
                    font-weight: bold;
                }

                a {
                    display: inline-block;
                    padding: 5px 0;
                }


            }



        }

        .card-price {
            background: #ffffff;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
            padding: 20px 40px;
            display: flex;
            gap: 20px;

            .card-service {
                display: flex;
                flex-direction: column;
                justify-content: space-between;

                .icon {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    padding: 10px;
                    width: 50px;
                    font-size: 20px;
                    font-weight: bold;
                    background: #30e351;
                    color: white;
                    border-radius: 5px;
                }

                p {
                    font-size: 14px;
                    font-weight: 700;
                    color: #6E757F;
                }

                .card-revenu {
                    font-size: 15px;
                    color: #30e351;
                    font-weight: bold;

                }

                h1 {
                    font-size: 28px;
                    font-weight: bold;
                }
            }

            .rotate {
                color: #035ECF;
                font-size: 20px;
                transform: rotate(90deg);
            }
        }

        .card-chart {
            background: #ffffff;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
            .apexcharts-menu-icon {
                display: none;
            }

            .apexcharts-yaxis {
                display: none;
            }

            .apexcharts-legend {
                display: none;
            }

            .apexcharts-xaxis {
                display: none;
            }

            .card-title {
                text-align: center;
                font-size: 25px;
                font-weight: bold;
                padding: 10px 0;
            }
        }
        .card-description{
            display: flex;
            flex-direction: column;
            gap: 20px;
           
            .card-detail{
                padding: 30px 100px;
                background: #ffffff;
                box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
                display: flex;
                justify-content: space-between;
                align-items: center;
                gap: 30px;
                height: 100%;
                h1 {
                    font-size: 20px;
                    font-weight: bold;
                }
                span {
                    font-size: 16px;
                    font-weight: bold;
                }   
            }
        }

    }



    .seller-content {
        display: flex;
        justify-content: space-between;

    }

    .seller-chart {

        .chart-rating {
            display: flex;
            justify-content: space-between;
            gap: 20px;

            .chart {
                margin-top: 40px;
                width: 50%;
                background: #ffffff;
                box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
            }
        }


        .apexcharts-toolbar {
            display: none;
        }
    }

    .seller-rating {
        margin-top: 20px;
        width: 50%;

        .service {
            display: flex;
            justify-content: space-between;

            .service-card {
                display: flex;
                justify-content: center;
                align-items: center;
                margin-top: 20px;
                padding: 10px 20px;
                background: #ffffff;
                border-radius: 5px;
                gap: 20px;
                box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);

                i {
                    padding: 15px;
                    background: #5822d6;
                    color: white;
                    border-radius: 5px;
                }

                .blue {
                    background: #5822d6;
                }

                .green {
                    background: #30e351;
                }

                .pink {
                    background: #e51286;
                }

                h3 {
                    font-size: 20px;
                    font-weight: bold;
                }

                span {
                    font-size: 14px;
                    font-weight: 700;
                    color: #6E757F;
                    font-family: "Archivo SemiExpanded", sans-serif;
                }
            }
        }

        .rating-content {
            background: #ffffff;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
            border-radius: 5px;
            padding: 20px 40px;
            margin-top: 20px;
        }

        .rating-content-title {
            font-size: 20px;
            font-weight: bold;
            color: black;
        }

        .rating {
            padding: 10px 0;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .rating-service {
                width: 100%;
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding-top: 5px;

                span {
                    font-size: 15px;
                    font-weight: bold;
                    color: #000;
                }

                .rating-title {
                    font-weight: 500;
                    color: #000;
                }
            }

            .rating-chart {
                width: 100%;
            }
        }

        .review-title {
            display: flex;
            justify-content: space-between;
            align-items: center;

            h1 {
                font-size: 24px;
                font-weight: bold;
            }
        }

        .review-rate {
            display: flex;
            justify-content: space-between;
            align-items: center;

        }

        .review-detail {
            font-size: 15px;
            font-weight: bold;
            color: #035ECF;
            cursor: pointer;
        }
    }
}
</style>