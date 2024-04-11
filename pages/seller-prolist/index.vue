<template>
    <div class="seller-prolist">
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
                        <el-option v-for="item in state.options" :key="item.value" :label="item.label"
                            :value="item.value">
                        </el-option>
                    </el-select>
                </div>
            </div>
        </div>

        <div class="seller-card">
            <div class="seller-content">
                <div class="seller-img">
                    <div class="card-img-item">
                        <img src="~assets/images/seller-prolist/8.webp" width="100" />
                    </div>
                </div>
                <div class="seller-btn">
                    <button class="seller-click">Profile</button>
                </div>
            </div>
            <div class="seller-title">
                <h1>Wood Cabins</h1>
                <address>
                    <nuxt-link class="link" to="">www.Website.com</nuxt-link>
                    <p style="max-width: 220px">
                        53 West Cherry Hill Lane Murfreesboro, TN 37128
                    </p>
                    <nuxt-link to="">+1(355) 896-8140</nuxt-link>
                    <nuxt-link to="">email@.com</nuxt-link>
                </address>
            </div>

            <div class="seller-square">
                <div class="square"></div>
            </div>
            <div class="seller-statistic">
                <div class="statistic">
                    <h1>Statistics:</h1>
                    <div class="statistic-icon">
                        <div class="icon"><i class="el-icon-sell"></i></div>
                        <div>
                            <h2>234</h2>
                            <p>New Order</p>
                        </div>
                    </div>
                    <div class="statistic-icon">
                        <div class="icon">
                            <i class="el-icon-coin money"></i>
                        </div>
                        <div>
                            <h2>$23k</h2>
                            <p>Income</p>
                        </div>
                    </div>
                    <div>
                        <h1>Review Rate:</h1>
                    </div>

                    <el-rate v-model="state.rate" disabled show-score text-color="#ff9900"
                        score-template="{value} points">
                    </el-rate>
                </div>
            </div>
            <div class="seller-rating">
                <div>Sales Profit by Category:</div>
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
            </div>
        </div>
        <div class="seller-card">
            <div class="seller-content">
                <div class="seller-img">
                    <div class="card-img-item">
                        <img src="~assets/images/seller-prolist/8.webp" width="100" />
                    </div>
                </div>
                <div class="seller-btn">
                    <button class="seller-click">Profile</button>
                </div>
            </div>
            <div class="seller-title">
                <h1>Wood Cabins</h1>
                <address>
                    <nuxt-link class="link" to="">www.Website.com</nuxt-link>
                    <p style="max-width: 220px">
                        53 West Cherry Hill Lane Murfreesboro, TN 37128
                    </p>
                    <nuxt-link to="">+1(355) 896-8140</nuxt-link>
                    <nuxt-link to="">email@.com</nuxt-link>
                </address>
            </div>

            <div class="seller-square">
                <div class="square"></div>
            </div>
            <div class="seller-statistic">
                <div class="statistic">
                    <h1>Statistics:</h1>
                    <div class="statistic-icon">
                        <div class="icon"><i class="el-icon-sell"></i></div>
                        <div>
                            <h2>234</h2>
                            <p>New Order</p>
                        </div>
                    </div>
                    <div class="statistic-icon">
                        <div class="icon">
                            <i class="el-icon-coin money"></i>
                        </div>
                        <div>
                            <h2>$23k</h2>
                            <p>Income</p>
                        </div>
                    </div>
                    <div>
                        <h1>Review Rate:</h1>
                    </div>

                    <el-rate v-model="state.rate" disabled show-score text-color="#ff9900"
                        score-template="{value} points">
                    </el-rate>
                </div>
            </div>
            <div class="seller-rating">
                <div>Sales Profit by Category:</div>
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
            </div>
        </div>
        <div class="seller-card">
            <div class="seller-content">
                <div class="seller-img">
                    <div class="card-img-item">
                        <img src="~assets/images/seller-prolist/8.webp" width="100" />
                    </div>
                </div>
                <div class="seller-btn">
                    <button class="seller-click">Profile</button>
                </div>
            </div>
            <div class="seller-title">
                <h1>Wood Cabins</h1>
                <address>
                    <nuxt-link class="link" to="">www.Website.com</nuxt-link>
                    <p style="max-width: 220px">
                        53 West Cherry Hill Lane Murfreesboro, TN 37128
                    </p>
                    <nuxt-link to="">+1(355) 896-8140</nuxt-link>
                    <nuxt-link to="">email@.com</nuxt-link>
                </address>
            </div>

            <div class="seller-square">
                <div class="square"></div>
            </div>
            <div class="seller-statistic">
                <div class="statistic">
                    <h1>Statistics:</h1>
                    <div class="statistic-icon">
                        <div class="icon"><i class="el-icon-sell"></i></div>
                        <div>
                            <h2>234</h2>
                            <p>New Order</p>
                        </div>
                    </div>
                    <div class="statistic-icon">
                        <div class="icon">
                            <i class="el-icon-coin money"></i>
                        </div>
                        <div>
                            <h2>$23k</h2>
                            <p>Income</p>
                        </div>
                    </div>
                    <div>
                        <h1>Review Rate:</h1>
                    </div>

                    <el-rate v-model="state.rate" disabled show-score text-color="#ff9900"
                        score-template="{value} points">
                    </el-rate>
                </div>
            </div>
            <div class="seller-rating">
                <div>Sales Profit by Category:</div>
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
            </div>
        </div>
        <div class="seller-card">
            <div class="seller-content">
                <div class="seller-img">
                    <div class="card-img-item">
                        <img src="~assets/images/seller-prolist/8.webp" width="100" />
                    </div>
                </div>
                <div class="seller-btn">
                    <button class="seller-click">Profile</button>
                </div>
            </div>
            <div class="seller-title">
                <h1>Wood Cabins</h1>
                <address>
                    <nuxt-link class="link" to="">www.Website.com</nuxt-link>
                    <p style="max-width: 220px">
                        53 West Cherry Hill Lane Murfreesboro, TN 37128
                    </p>
                    <nuxt-link to="">+1(355) 896-8140</nuxt-link>
                    <nuxt-link to="">email@.com</nuxt-link>
                </address>
            </div>

            <div class="seller-square">
                <div class="square"></div>
            </div>
            <div class="seller-statistic">
                <div class="statistic">
                    <h1>Statistics:</h1>
                    <div class="statistic-icon">
                        <div class="icon"><i class="el-icon-sell"></i></div>
                        <div>
                            <h2>234</h2>
                            <p>New Order</p>
                        </div>
                    </div>
                    <div class="statistic-icon">
                        <div class="icon">
                            <i class="el-icon-coin money"></i>
                        </div>
                        <div>
                            <h2>$23k</h2>
                            <p>Income</p>
                        </div>
                    </div>
                    <div>
                        <h1>Review Rate:</h1>
                    </div>

                    <el-rate v-model="state.rate" disabled show-score text-color="#ff9900"
                        score-template="{value} points">
                    </el-rate>
                </div>
            </div>
            <div class="seller-rating">
                <div>Sales Profit by Category:</div>
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
            </div>
        </div>

        <div class="pagination">
            <el-pagination background layout="prev, pager, next" :total="30">
            </el-pagination>
        </div>
    </div>
</template>


<script>
import { defineComponent, reactive, ref } from '@nuxtjs/composition-api'

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
.seller-prolist {
    padding: 0 30px;

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

    .seller-card {
        margin-top: 20px;
        display: flex;
        width: 100%;
        background: #ffffff;

        .seller-content {
            padding: 20px 20px;

            .seller-img {
                padding: 20px 40px;
                background: #ffffff;
                border: 1px solid rgba(0, 0, 0, 0.1);
            }

            .seller-btn {
                padding: 20px 0;
                margin-top: 40px;

                .seller-click {
                    padding: 10px 15px;
                    width: 100%;
                    border: none;
                    border-radius: 20px;
                    background-color: #00ba9d;
                    border: 1px solid #01c8a9;
                    font-weight: bold;
                    color: #fff;
                    box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
                }
            }
        }
    }

    .seller-title {
        padding: 10px 10px;

        h1 {
            font-size: 30px;
            font-weight: bold;
        }

        a {
            display: block;
            padding: 5px 0;
        }

        .link {
            color: blue;
        }
    }

    .seller-square {
        padding: 20px 10px;

        .square {
            width: 250px;
            height: 100%;
            background: #f9f9f9;
        }
    }

    .seller-statistic {
        padding: 20px 10px;

        .statistic {
            display: flex;
            flex-direction: column;

            h1 {
                font-size: 20px;
                font-weight: bold;
            }

            .statistic-icon {
                display: flex;
                gap: 10px;

                i {
                    margin-top: 10px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 50px;
                    height: 50px;
                    background: #00ba9d;
                    color: white;
                    font-size: 20px;
                    font-weight: bold;
                    border-radius: 5px;
                }

                p {
                    font-size: 14px;
                    font-weight: 400;
                }

                .money {
                    margin-top: 10px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 50px;
                    height: 50px;
                    background: #035ecf;
                    color: white;
                    font-size: 20px;
                    font-weight: bold;
                    border-radius: 5px;
                }
            }

            .el-rate__icon {
                font-size: 25px;
            }

            .el-rate__text {
                display: none;
            }
        }
    }

    .seller-rating {
        padding: 20px 40px;
        width: 100%;

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
    }
    .pagination {
        padding: 20px 0;
    }
}
</style>
