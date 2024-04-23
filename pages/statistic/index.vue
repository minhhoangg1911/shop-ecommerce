<template>
  <div class="statistic">
    <div class="statistic-container">
      <div class="left">
        <div>
          <h5 class="title">General Income Statistics</h5>
          <table>
            <thead>
              <tr>
                <th>year</th>
                <th>customers</th>
                <th>trend</th>
                <th>revenue</th>
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
        </div>
        <div class="total">
          <i class="el-icon-orange"></i>
          <div>
            <h5>$924k</h5>
            <span>Total income</span>
          </div>
        </div>
        <div class="seller-rating">
          <div class="rating-content">
            <div class="rating-content-title">Income level by city</div>
            <div class="rating">
              <div class="rating-chart">
                <div class="rating-service">
                  <div class="rating-title">New York</div>
                  <span>$123k</span>
                </div>
                <el-progress
                  :text-inside="true"
                  :stroke-width="15"
                  :percentage="30"
                  color="#00BA9D"
                ></el-progress>
              </div>
            </div>

            <div class="rating">
              <div class="rating-chart">
                <div class="rating-service">
                  <div class="rating-title">Los Angeles</div>
                  <span>$89k</span>
                </div>
                <el-progress
                  :text-inside="true"
                  :stroke-width="15"
                  :percentage="20"
                  status="success"
                  color="#00193B"
                ></el-progress>
              </div>
            </div>
            <div class="rating">
              <div class="rating-chart">
                <div class="rating-service">
                  <div class="rating-title">Houston</div>
                  <span>$67k</span>
                </div>
                <el-progress
                  :text-inside="true"
                  :stroke-width="15"
                  :percentage="50"
                  status="warning"
                  color="#FF5470"
                ></el-progress>
              </div>
            </div>
            <div class="rating">
              <div class="rating-chart">
                <div class="rating-service">
                  <div class="rating-title">Dallas</div>
                  <span>$23k</span>
                </div>
                <el-progress
                  :text-inside="true"
                  :stroke-width="15"
                  :percentage="25"
                  status="exception"
                  color="#00BA9D"
                ></el-progress>
              </div>
            </div>
            <div class="rating">
              <div class="rating-chart">
                <div class="rating-service">
                  <div class="rating-title">Chicago</div>
                  <span>$15k</span>
                </div>
                <el-progress
                  :text-inside="true"
                  :stroke-width="15"
                  :percentage="25"
                  status="exception"
                  color="#00193B"
                ></el-progress>
              </div>
            </div>
            <div class="rating">
              <div class="rating-chart">
                <div class="rating-service">
                  <div class="rating-title">Madrid</div>
                  <span>$10k</span>
                </div>
                <el-progress
                  :text-inside="true"
                  :stroke-width="15"
                  :percentage="25"
                  status="exception"
                  color="#FF5470"
                ></el-progress>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="right">
        <div>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d125442.5041766752!2d106.67932820143434!3d10.728447617798139!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1svi!2s!4v1713848991678!5m2!1svi!2s"
            width="100%"
            height="680px"
            style="border: 0"
            border-radius="5px"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({
  setup() {},
});
</script>

<style lang="scss">
.statistic {
  padding: 20px 30px;
  .statistic-container {
    display: flex;
    background: #fff;
    padding: 20px 30px;
    box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
    border-radius: 5px;
    width: 100%;
    gap: 20px;
    .left {
      flex-grow: 1;
      .title {
        padding: 10px;
        font-size: 20px;
      }
      table {
        thead {
          tr {
            th {
              padding: 10px;
              font-size: 10px;
              font-weight: 500;
              text-transform: uppercase;
              color: #8d8d99;
              text-align: left;
              font-family: "Archivo", sans-serif;
              height: 23px;
            }
          }
        }
        tbody {
          tr {
            td {
              padding: 10px;
              font-family: "Archivo SemiExpanded", sans-serif;
              font-weight: 700;
              color: #00193b;
              font-size: 14px;
              border-collapse: collapse;
            }
          }
          .line {
            border-bottom: 1px solid #e2e1e1;
          }
        }
      }
      .total {
        padding: 10px;
        display: flex;
        align-items: center;
        gap: 20px;

        div {
          display: flex;
          flex-direction: column;
          h5 {
            padding: 0 !important;
            font-size: 28px;
            font-weight: bold;
          }
          span {
            font-size: 14px;
            font-weight: 700;
            font-family: "Archivo SemiExpanded", sans-serif;
            color: #6e757f;
          }
        }

        i {
          padding: 15px;
          background: #035ecf;
          color: white;
          border-radius: 5px;
        }
      }
      .seller-rating {
        margin-top: 20px;

        .service {
          display: flex;
          justify-content: space-between;
        }

        .rating-content {
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
          .el-progress-bar__innerText {
            display: none;
          }
        }
      }
    }
    .right {
      flex-grow: 13;
      padding: 20px;
      iframe {
        border-radius: 10px;
      }
    }
  }
}
</style>
