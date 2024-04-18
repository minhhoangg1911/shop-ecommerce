<template>
  <div class="order">
    <div class="sale-period">
      <div class="date">
        <div><h4>Sales period</h4></div>
        <el-date-picker
          v-model="value"
          type="datetimerange"
          start-placeholder="Start Date"
          range-separator="-"
          end-placeholder="End Date"
          :default-time="['12:00:00']"
        >
        </el-date-picker>
      </div>
      <div class="select">
        <div>
          <el-select v-model="state.value1" clearable placeholder="Select">
            <el-option
              v-for="item in state.options"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
        <div>
          <el-select v-model="state.value1" clearable placeholder="Select">
            <el-option
              v-for="item in state.options"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
      </div>
    </div>
    <div class="order-grid">
      <div class="seller-rating">
        <div class="seller-title">Average Rate (%)</div>
        <div class="rating">
          <div class="rating-chart">
            <div class="rating-service">
              <div class="rating-title">Referral Program Budget</div>
              <span>27%</span>
            </div>
            <el-progress
              :text-inside="true"
              :stroke-width="26"
              :percentage="30"
            ></el-progress>
          </div>
        </div>

        <div class="rating">
          <div class="rating-chart">
            <div class="rating-service">
              <div class="rating-title">Referral Rate by Campaign</div>
              <span>52%</span>
            </div>
            <el-progress
              :text-inside="true"
              :stroke-width="22"
              :percentage="50"
              status="warning"
            ></el-progress>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="card-item">
          <div class="icon">
            <i class="el-icon-s-claim"></i>
          </div>
          <i class="el-icon-more rotate"></i>
        </div>
        <div>
          <h6>Orders Completed</h6>
        </div>
        <div>
          <span>2,345</span>
        </div>
      </div>
      <div class="card">
        <div class="card-item">
          <div class="icon green">
            <i class="el-icon-s-claim green"></i>
          </div>
          <i class="el-icon-more rotate"></i>
        </div>
        <div>
          <h6>Orders Completed</h6>
        </div>
        <div>
          <span>2,345</span>
        </div>
      </div>
      <div class="card">
        <div class="card-item">
          <div class="icon red">
            <i class="el-icon-s-claim red"></i>
          </div>
          <i class="el-icon-more rotate"></i>
        </div>
        <div>
          <h6>Orders Completed</h6>
        </div>
        <div>
          <span>2,345</span>
        </div>
      </div>
      <div class="card">
        <div class="card-item">
          <div class="icon black">
            <i class="el-icon-s-claim black"></i>
          </div>
          <i class="el-icon-more rotate"></i>
        </div>
        <div>
          <h6>Orders Completed</h6>
        </div>
        <div>
          <span>2,345</span>
        </div>
      </div>
    </div>
    <div class="table">
      <el-table :data="state.tableData" style="width: 100%">
        <el-table-column prop="order" label="#order" width="180">
          <div>#123456</div>
        </el-table-column>
        <el-table-column prop="product" label="product" width="180">
          <div class="product-image">
            <img
              src="~assets/images/top-products/1.webp"
              width="50"
              height="50"
            />
            <div>
              <h5 style="font-size: 15px">Oculus Quest 2 VR Headset 64 GB</h5>
              <span>Regular price: $600</span>
              <span>Sale price: $559</span>
            </div>
          </div>
        </el-table-column>
        <el-table-column prop="sku" label="sku">
          <div>123456FR</div>
        </el-table-column>
        <el-table-column prop="category" label="category">
          <div class="product-category">
            <div><i class="el-icon-s-tools"></i></div>
            <span>Electronics</span>
          </div>
        </el-table-column>
        <el-table-column prop="payment" label="payment">
          <div class="product-payment">
            <h5>$600</h5>
            <span>full paid</span>
          </div>
        </el-table-column>
        <el-table-column prop="status" label="status">
          <div class="product-status">
            <button>Complete</button>
          </div>
        </el-table-column>
        <el-table-column prop="rate" label="rate">
          <div>
            <div class="block">
              <el-rate v-model="value3"></el-rate>
            </div>
          </div>
        </el-table-column>
        <el-table-column prop="actions" label="actions">
          <div class="product-actions">
            <button><i class="el-icon-edit-outline edit"></i></button>
            <button><i class="el-icon-more rotate"></i></button>
          </div>
        </el-table-column>
      </el-table>
    </div>
    <div>
      <el-pagination background layout="prev, pager, next" :total="20">
      </el-pagination>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive, ref } from '@nuxtjs/composition-api'
import SalePeriod from '~/components/SalePeriod/SalePeriod.vue'
export default defineComponent({
  comments: {
    SalePeriod,
  },
  setup() {
    const value = ref('')
    const value3 = ref(null)
    const state = reactive({
      options: [
        {
          value: 'Option1',
          label: 'Option1',
        },
        {
          value: 'Option2',
          label: 'Option2',
        },
        {
          value: 'Option3',
          label: 'Option3',
        },
        {
          value: 'Option4',
          label: 'Option4',
        },
        {
          value: 'Option5',
          label: 'Option5',
        },
      ],

      value1: '',
      tableData: [
        {
          order: '2016-05-03',
          product: 'Tom',
          sku: 'No. 189, Grove St, Los Angeles',
          category: '',
          payment: '',
          status: '',
          rate: '',
          actions: '',
        },
        {
          order: '2016-05-03',
          product: 'Tom',
          sku: 'No. 189, Grove St, Los Angeles',
          category: '',
          payment: '',
          status: '',
          rate: '',
          actions: '',
        },
        {
          order: '2016-05-03',
          product: 'Tom',
          sku: 'No. 189, Grove St, Los Angeles',
          category: '',
          payment: '',
          status: '',
          rate: '',
          actions: '',
        },
        {
          order: '2016-05-03',
          product: 'Tom',
          sku: 'No. 189, Grove St, Los Angeles',
          category: '',
          payment: '',
          status: '',
          rate: '',
          actions: '',
        },
        {
          order: '2016-05-03',
          product: 'Tom',
          sku: 'No. 189, Grove St, Los Angeles',
          category: '',
          payment: '',
          status: '',
          rate: '',
          actions: '',
        },
        {
          order: '2016-05-03',
          product: 'Tom',
          sku: 'No. 189, Grove St, Los Angeles',
          category: '',
          payment: '',
          status: '',
          rate: '',
          actions: '',
        },
      ],
    })
    return { value, state, value3 }
  },
})
</script>

<style lang="scss">
.order {
  padding: 20px 30px;
  .sale-period {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .select {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
    }
  }
  .order-grid {
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(6, minmax(0, 1fr));
    .seller-rating {
      display: grid;
      grid-column: span 2 / span 2;
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
    }
    .card {
      padding: 10px;
      margin-top: 20px;
      .card-item {
        display: flex;
        justify-content: space-between;
        padding: 20px;
        .icon {
          padding: 10px;
          border-radius: 5px;
          font-size: 20px;
          background: #035ecf;
          color: white;
        }
        .rotate {
          transform: rotate(90deg);
          color: #035ecf;
          font-size: 20px;
        }
        .black {
          background: #515c6b;
        }
        .red {
          background: #ff5470;
        }
        .green {
          background: #00ba9d;
        }
      }
      h6 {
        color: #00193b;
        font-weight: 700;
        padding: 20px;
      }
      span {
        padding: 20px;
        font-size: 28px;
        font-weight: bold;
        color: #000;
      }
    }
  }
  .table {
    .el-table thead {
      color: #2f64cd;
      font-weight: 500;
      text-transform: uppercase;
      font-weight: bold;
      font-size: 12px;
      font-family: 'Archivo SemiExpanded', sans-serif;
    }
    .product-image {
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }
    .product-category {
      display: flex;
      align-items: center;
      gap: 10px;
      div {
        padding: 10px;
        background: #2f64cd;
        border-radius: 5px;
        i {
          color: white;
        }
      }
    }
    .product-payment {
      display: flex;
      flex-direction: column;
    }
    .product-status {
      background: #035ecf;
      width: 134px;
      height: 40px;
      font-size: 14px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      line-height: 1;
      border-radius: 20px;
      color: #fff;
      button {
        text-transform: uppercase;
        border: none;
        background: none;
        color: #fff;
        font-family: inherit;
      }
    }
    .product-actions {
      display: flex;
      gap: 20px;
      button {
        background: none;
        border: none;
      }
      .edit {
        padding: 10px;
        font-size: 20px;
        font-weight: bold;
        background: #2f64cd;
        color: white;
      }
      .rotate {
        transform: rotate(90deg);
        font-size: 20px;
        color: #2f64cd;
      }
    }
  }
}
</style>
