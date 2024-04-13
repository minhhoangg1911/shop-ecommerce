<template>
    <div class="revenue-page">
        <SalePeriod />
        <div class="revenue">
            <div class="revenue-grid">
                <div class="revenue-chart">
                    <client-only>
                        <apex-chart type="line" height="350" :options="state.data.chartOptions"
                            :series="state.data.series"></apex-chart>
                    </client-only>
                </div>
                <div class="revenue-content">
                    <div class="revenue-card">
                        <div class="revenue-icon">
                            <i class="el-icon-money left yellow "></i>
                            <i class="el-icon-more right"></i>
                        </div>
                        <div class="revenue-excess">
                            <span>Income 2022</span>
                            <div class="revenue-price">
                                <i class="el-icon-caret-top"></i>
                                <span>+78%</span>
                            </div>
                        </div>
                        <span>$96.1k</span>
                    </div>
                    <div class="revenue-card">
                        <div class="revenue-icon">
                            <i class="el-icon-money left pink"></i>
                            <i class="el-icon-more right"></i>
                        </div>
                        <div class="revenue-excess">
                            <span>Income 2022</span>
                            <div class="revenue-price">
                                <i class="el-icon-caret-top"></i>
                                <span>+78%</span>
                            </div>
                        </div>
                        <span>$96.1k</span>
                    </div>
                    <div class="revenue-card">
                        <div class="revenue-icon">
                            <i class="el-icon-money left blue"></i>
                            <i class="el-icon-more right"></i>
                        </div>
                        <div class="revenue-excess">
                            <span>Income 2022</span>
                            <div class="revenue-price red">
                                <i class="el-icon-caret-top"></i>
                                <span>+78%</span>
                            </div>
                        </div>
                        <span>$96.1k</span>
                    </div>
                    <div class="revenue-card">
                        <div class="revenue-icon">
                            <i class="el-icon-money left green"></i>
                            <i class="el-icon-more right"></i>
                        </div>
                        <div class="revenue-excess">
                            <span>Income 2022</span>
                            <div class="revenue-price">
                                <i class="el-icon-caret-top"></i>
                                <span>+78%</span>
                            </div>
                        </div>
                        <span>$96.1k</span>
                    </div>

                </div>
                <div class="revenue-chart-pie">
                    <div class="pie-title">Profit Performance</div>
                    <client-only>
                        <apex-chart type="pie" width="380" :options="state.dataPie.chartOptions"
                            :series="state.dataPie.series">
                        </apex-chart>
                    </client-only>
                    <div class="revenue-year">
                        <div class="revenue-circle">
                            <div>
                                <span class="revenue-green"></span>
                            </div>
                            <div>2022</div>
                        </div>
                        <div class="revenue-circle">
                            <div>
                                <span class="revenue-blue"></span>
                            </div>
                            <div>2023</div>
                        </div>
                    </div>
                </div>

                <div class="revenue-conversion">
                    <div class="tables">
                        <div>
                            <h4>Conversion Rate</h4>
                        </div>
                        <table>
                            <thead>
                                <tr>
                                    <th>Year</th>
                                    <th>Customers</th>
                                    <th>Trend</th>
                                    <th>Revenue</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr class="line">
                                    <td>2022</td>
                                    <td>3,234</td>
                                    <td>$10%</td>
                                    <td>$124k</td>
                                </tr>

                                <tr>
                                    <td>2022</td>
                                    <td>3,234</td>
                                    <td>$10%</td>
                                    <td>$124k</td>
                                </tr>
                            </tbody>
                        </table>
                        <div class="revenue-description">
                            <div>
                                <h1>32,547</h1>
                                <span>Regular Customers</span>
                                <div class="revenue-icon">
                                    <i class="el-icon-caret-top icon"></i>
                                    <span>+14,08%</span>
                                </div>
                            </div>
                            <div>
                                <h1>32,547</h1>
                                <span>Regular Customers</span>
                                <div class="revenue-icon">
                                    <i class="el-icon-caret-top icon"></i>
                                    <span>+14,08%</span>
                                </div>
                            </div>

                        </div>
                    </div>

                </div>
                <div class="revenue-rating">
                    <div class="seller-rating">

                        <div class="seller-title">Average Referral Rate</div>
                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Referral Program Budget</div>
                                    <span>27%</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="26" :percentage="30"></el-progress>
                            </div>
                        </div>

                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Referral Rate by 100 Purchased</div>
                                    <span>67%</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="24" :percentage="20"
                                    status="success"></el-progress>
                            </div>
                        </div>
                        <div class="rating">
                            <div class="rating-chart">
                                <div class="rating-service">
                                    <div class="rating-title">Referral Rate by Campaign</div>
                                    <span>52%</span>
                                </div>
                                <el-progress :text-inside="true" :stroke-width="22" :percentage="50"
                                    status="warning"></el-progress>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="revenue-total">
                    <div class="revenue-item">
                        <h4>Total Blance</h4>
                        <span>$176.2k</span>
                    </div>
                    <div class="revenue-item">
                        <h4>Total Blance</h4>
                        <span>$176.2k</span>
                    </div>
                    <div class="revenue-item">
                        <h4>Total Blance</h4>
                        <span>$176.2k</span>
                    </div>
                    <div></div>
                    <div></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent, reactive } from '@nuxtjs/composition-api'
import SalePeriod from '~/components/SalePeriod/SalePeriod.vue';

export default defineComponent({
    components: {
        SalePeriod,
    },
    setup() {
        const state = reactive({

            dataPie: {
                series: [70, 40],
                chartOptions: {
                    chart: {
                        width: 380,
                        type: 'pie',
                    },
                    labels: ['Team A', 'Team B', 'Team C', 'Team D', 'Team E'],
                    responsive: [{
                        breakpoint: 480,
                        options: {
                            chart: {
                                width: 200
                            },
                            legend: {
                                position: 'bottom'
                            }
                        }
                    }]
                },


            },

            data: {

                series: [{
                    name: "Session Duration",
                    data: [45, 52, 38, 24,]
                },
                {
                    name: "Page Views",
                    data: [35, 41, 62, 42,]
                },

                ],
                chartOptions: {
                    chart: {
                        height: 350,
                        type: 'line',
                        zoom: {
                            enabled: false
                        },
                    },
                    dataLabels: {
                        enabled: false
                    },
                    stroke: {
                        width: [5, 7, 5],
                        curve: 'straight',
                        dashArray: [0, 8, 5]
                    },
                    title: {
                        text: 'Page Statistics',
                        align: 'left'
                    },
                    legend: {
                        tooltipHoverFormatter: function (val, opts) {
                            return val + ' - <strong>' + opts.w.globals.series[opts.seriesIndex][opts.dataPointIndex] + '</strong>'
                        }
                    },
                    markers: {
                        size: 0,
                        hover: {
                            sizeOffset: 6
                        }
                    },
                    xaxis: {
                        categories: ['Q1', 'Q2', "Q3", "Q4"],
                    },
                    tooltip: {
                        y: [
                            {
                                title: {
                                    formatter: function (val) {
                                        return val + " (mins)"
                                    }
                                }
                            },
                            {
                                title: {
                                    formatter: function (val) {
                                        return val + " per session"
                                    }
                                }
                            },
                            {
                                title: {
                                    formatter: function (val) {
                                        return val;
                                    }
                                }
                            }
                        ]
                    },
                    grid: {
                        borderColor: '#f1f1f1',
                    }
                },


            },
        })
        return { state }
    },
})
</script>

<style lang="scss">
.revenue-page {
    padding: 0 30px;

    span {
        font-size: 14px;
        color: #6E757F;
        font-weight: 700;
        padding: 0;

    }

}

.revenue {
    padding: 30px 0;


    .revenue-grid {
        display: grid;
        grid-template-columns: auto auto auto;

        .revenue-chart {
            background: #ffffff;
            margin-right: 20px;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
        }

        .revenue-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            justify-content: space-between;
            gap: 20px;

            .revenue-card {
                background: #ffffff;
                box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
                padding: 20px 0;

                .revenue-icon {
                    padding: 0 20px;
                    display: flex;
                    justify-content: space-between;
                    align-items: center;

                    .left {
                        padding: 10px;
                        background: blue;
                        color: white;
                        border-radius: 5px;
                        font-size: 25px;
                    }

                    .right {
                        font-size: 25px;
                        transform: rotate(90deg);
                        color: blue;

                    }

                    .yellow {
                        background: #F8D518;
                    }

                    .pink {
                        background: #FF5470;
                    }

                    .blue {
                        background: #035ECF;
                    }

                    .green {
                        background: #00BA9D;
                    }
                }

                .revenue-excess {
                    padding: 0 20px;
                    display: flex;
                    justify-content: space-between;
                    margin-top: 30px;
                    margin-bottom: 10px;

                    span {
                        font-size: 14px;
                        color: #6E757F;
                        font-weight: 700;
                        padding: 0;

                    }

                    .revenue-price {
                        color: green;

                        span {
                            color: green;
                        }
                    }

                    .red {
                        color: #FF5470;


                        span {
                            color: #FF5470;
                        }
                    }
                }

                span {
                    font-size: 23px;
                    font-weight: bold;
                    padding: 10px 20px;

                }
            }
        }

        .revenue-chart-pie {
            margin-left: 20px;
            background: #ffffff;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
            padding: 0 20px;

            .apexcharts-legend {
                display: none;
            }

            .apexcharts-canvas {
                padding: 10px 20px;
            }

            .pie-title {
                text-align: center;
                font-size: 20px;
                font-weight: bold;
            }

            .revenue-year {

                width: 100%;
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 30px;

                div {
                    padding: 10px 5px;
                }

                .revenue-circle {
                    display: flex;
                    justify-content: center;
                    align-items: center;

                    .revenue-green {
                        display: inline-block;
                        width: 20px;
                        height: 20px;
                        background: rgb(0, 227, 150);
                        border-radius: 100%;
                    }

                    .revenue-blue {
                        display: inline-block;
                        width: 20px;
                        height: 20px;
                        background: rgb(0, 143, 251);
                        border-radius: 100%;
                    }
                }

            }
        }

        .revenue-conversion {
            margin-top: 20px;
            margin-right: 20px;
            padding: 20px 0;
            background: #ffffff;
            box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);

            .tables {
                padding: 0 10px;
            }

            h4 {
                padding: 0 10px;
                font-weight: bold;
            }

            table {

                th {
                    padding: 0 20px;
                    font-size: 10px;
                    font-weight: 500;
                    text-transform: uppercase;
                    color: #8D8D99;
                    text-align: left;
                    height: 23px;
                }

                td {
                    padding: 10px 20px;
                    font-size: 20px;
                    font-weight: bold;
                }

                .line {

                    border-bottom: 1px solid rgba(0, 0, 0, 0.3);
                }

            }

            .revenue-description {
                padding: 0 20px;
                display: flex;
                gap: 80px;

                h1 {
                    font-size: 28px;
                    font-weight: bold;
                }

                .revenue-icon {
                    padding: 20px 0px;
                    color: #00BA9D;

                    span {
                        color: #00BA9D;
                    }
                }

            }
        }

        .revenue-rating {
            .seller-rating {
                padding: 20px 20px;
                margin-top: 20px;
                background: #ffffff;
                box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);

                .seller-title {
                    font-size: 20px;
                    font-weight: bold;
                }

                .rating {
                    padding: 10px 0;
                    width: 100%;
                    display: flex;
                    justify-content: space-between;
                    align-items: center;

                    .el-progress-bar__inner {
                        background: #00193B;
                    }

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
                            padding: 10px 0;
                            font-weight: 500;
                            color: #000;
                        }
                    }

                    .rating-chart {
                        width: 100%;
                    }
                }
            }
        }

        .revenue-total {
            margin-top: 20px;
            margin-left: 20px;
            display: flex;
            flex-direction: column;
            height: 100%;
            .revenue-item {
                background: #ffffff;
                box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
                margin-bottom: 20px;
                padding: 20px 40px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                width: 100%;
                height: 100%;
                h4 {
                    font-size: 14px;
                    font-weight: bold;
                } 
                span {
                    font-size: 14px;
                    font-weight: bold;
                    color: black;
                }
            }
        }


    }



}
</style>
