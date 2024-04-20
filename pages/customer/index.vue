<template>
  <div class="customer">
    <div class="customer-rate">
      <div class="item">
        <div class="green">
          <i class="el-icon-s-custom"></i>
        </div>
        <h5>32,987</h5>
        <span>All</span>
      </div>
      <div class="item">
        <div class="blue">
          <i class="el-icon-s-custom"></i>
        </div>
        <h5>32,987</h5>
        <span>All</span>
      </div>
      <div class="item">
        <div class="red">
          <i class="el-icon-s-custom"></i>
        </div>
        <h5>32,987</h5>
        <span>All</span>
      </div>

      <div class="customer-conversion">
        <div class="revenue-conversion">
          <div>
            <h4>Conversion Rate</h4>
          </div>
          <div class="tables">
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
      </div>
    </div>
    <div class="customer-chart">
      <div class="revenue-chart-pie">
        <div class="pie-title">Profit Performance</div>
        <client-only>
          <apex-chart
            type="pie"
            width="380"
            :options="state.dataPie.chartOptions"
            :series="state.dataPie.series"
          >
          </apex-chart>
        </client-only>
      </div>
      <div class="revenue-rating">
        <div class="seller-rating">
          <div class="seller-title">Demographic segmentation by Age</div>
          <div class="rating">
            <div class="rating-chart">
              <div class="rating-service">
                <div class="rating-title">Age 18-25</div>
                <span>6,680</span>
              </div>
              <el-progress
                :text-inside="true"
                :stroke-width="18"
                :percentage="30"
              ></el-progress>
            </div>
          </div>

          <div class="rating">
            <div class="rating-chart">
              <div class="rating-service">
                <div class="rating-title">Age 25-45</div>
                <span>15,234</span>
              </div>
              <el-progress
                :text-inside="true"
                :stroke-width="18"
                :percentage="55"
                status="success"
              ></el-progress>
            </div>
          </div>
          <div class="rating">
            <div class="rating-chart">
              <div class="rating-service">
                <div class="rating-title">Age 45-65</div>
                <span>2,034</span>
              </div>
              <el-progress
                :text-inside="true"
                :stroke-width="18"
                :percentage="10"
                status="warning"
              ></el-progress>
            </div>
          </div>
          <div class="rating">
            <div class="rating-chart">
              <div class="rating-service">
                <div class="rating-title">Age over 65</div>
                <span>792</span>
              </div>
              <el-progress
                :text-inside="true"
                :stroke-width="18"
                :percentage="5"
                status="warning"
              ></el-progress>
            </div>
          </div>
          <div class="gender">
            <div class="gender-item">
              <div class="item">
                <i class="el-icon-user"></i>
                <span>65%</span>
              </div>
              <div class="item">
                <i class="el-icon-user"></i>
                <span>65%</span>
              </div>
              <div class="item">
                <i class="el-icon-user"></i>
                <span>65%</span>
              </div>
            </div>
            <p>
              Nullam sodales rutrum arcu. Maecenas sed lorem ut dolor tincidunt mattis
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive } from "@nuxtjs/composition-api";

export default defineComponent({
  setup() {
    const state = reactive({
      dataPie: {
        series: [70, 40, 20, 10],
        chartOptions: {
          chart: {
            width: 380,
            type: "pie",
          },
          labels: ["Team A", "Team B", "Team C", "Team D"],
          responsive: [
            {
              breakpoint: 480,
              options: {
                chart: {
                  width: 200,
                },
                legend: {
                  position: "bottom",
                },
              },
            },
          ],
        },
      },

      data: {
        series: [
          {
            name: "Session Duration",
            data: [45, 52, 38, 24],
          },
          {
            name: "Page Views",
            data: [35, 41, 62, 42],
          },
        ],
        chartOptions: {
          chart: {
            height: 350,
            type: "line",
            zoom: {
              enabled: false,
            },
          },
          dataLabels: {
            enabled: false,
          },
          stroke: {
            width: [5, 7, 5],
            curve: "straight",
            dashArray: [0, 8, 5],
          },
          title: {
            text: "Page Statistics",
            align: "left",
          },
          legend: {
            tooltipHoverFormatter: function (val, opts) {
              return (
                val +
                " - <strong>" +
                opts.w.globals.series[opts.seriesIndex][opts.dataPointIndex] +
                "</strong>"
              );
            },
          },
          markers: {
            size: 0,
            hover: {
              sizeOffset: 6,
            },
          },
          xaxis: {
            categories: ["Q1", "Q2", "Q3", "Q4"],
          },
          tooltip: {
            y: [
              {
                title: {
                  formatter: function (val) {
                    return val + " (mins)";
                  },
                },
              },
              {
                title: {
                  formatter: function (val) {
                    return val + " per session";
                  },
                },
              },
              {
                title: {
                  formatter: function (val) {
                    return val;
                  },
                },
              },
            ],
          },
          grid: {
            borderColor: "#f1f1f1",
          },
        },
      },
    });
    return { state };
  },
});
</script>

<style lang="scss">
.customer {
  padding: 20px 30px;
  .customer-rate {
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(6, 1fr);
    .item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
      gap: 10px;
      border-radius: 5px;
      background: #fff;
      box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
      div {
        padding: 10px 15px;
        border-radius: 5px;
        color: #fff;
        font-size: 20px;
      }
      h5 {
        font-size: 26px;
        font-weight: bold;
      }
      span {
        font-weight: bold;
      }
      .green {
        background: #00ba9d;
      }
      .blue {
        background: #035ecf;
      }
      .red {
        background: #ff5470;
      }
    }
    .customer-conversion {
      grid-column: span 3 / span 3;
      .revenue-conversion {
        padding: 20px 0;
        background: #ffffff;
        box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
        div {
          h4 {
            padding: 0 30px;
          }
        }
        .tables {
          padding: 0 10px;
          display: flex;
          gap: 20px;
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
            color: #8d8d99;
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
            color: #00ba9d;

            span {
              color: #00ba9d;
            }
          }
        }
      }
    }
  }
  .customer-chart {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 20px;
    .revenue-chart-pie {
      margin-top: 20px;
      grid-column: span 4 / span 4;
      background: #fff;
      .pie-title {
        font-size: 28px;
        font-weight: bold;
        padding: 10px 20px;
      }
    }
    .revenue-rating {
      grid-column: span 2 / span 2;
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
            background: #00193b;
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
        .gender {
          .gender-item {
            display: flex;
            gap: 20px;
            .item {
              display: flex;
              flex-direction: column;
              padding: 10px 0;
              i {
                padding: 10px;
                background: #035ecf;
                border-radius: 5px;
                color: #fff;
              }
              span {
                font-size: 20px;
                font-weight: bold;
              }
            }
          }
        }
      }
    }
  }
}
</style>
