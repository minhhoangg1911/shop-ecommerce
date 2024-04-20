<template>
  <div class="transaction">
    <ViewPageProfile />
    <div class="transaction-table">
      <el-table :data="state.tableData" style="width: 100%">
        <el-table-column prop="date" label="Date" width="180">
          <div class="date">
            <i class="el-icon-alarm-clock"></i>
            <div>
              <div><span class="h6">05/04/2024</span></div>
              <div><span> at 08:34 PM</span></div>
            </div>
          </div>
        </el-table-column>
        <el-table-column prop="seller" label="seller" width="180">
          <div class="seller">
            <div>
              <img src="~assets/images/seller-grid/4.webp" width="50" />
            </div>
            <div>Ecom</div>
          </div>
        </el-table-column>
        <el-table-column prop="sku" label="sku">
          <div>62241</div>
        </el-table-column>
        <el-table-column prop="type" label="type">
          <div>invoice</div>
        </el-table-column>
        <el-table-column prop="status" label="status">
          <div class="status">
            <button>Approved</button>
          </div>
        </el-table-column>
        <el-table-column prop="curr" label="curr">
          <div>AWG</div>
        </el-table-column>
        <el-table-column prop="fee" label="fee">
          <div>3927.56</div>
        </el-table-column>
        <el-table-column prop="tax" label="tax">
          <div>1.0</div>
        </el-table-column>
        <el-table-column prop="total" label="total">
          <div class="total">$3888.28</div>
        </el-table-column>
      </el-table>
    </div>
    <div class="pagination">
      <el-pagination background layout="prev, pager, next" :total="20"> </el-pagination>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive } from "@nuxtjs/composition-api";
import ViewPageProfile from "~/components/ViewProfile/ViewPageProfile.vue";
export default defineComponent({
  components: {
    ViewPageProfile,
  },
  setup() {
    const state = reactive({
      tableData: [
        {
          date: "2016-05-03",
          seller: "Tom",
          sku: "No. 189, Grove St, Los Angeles",
          type: "No. 189, Grove St, Los Angeles",
          status: "No. 189, Grove St, Los Angeles",
          curr: "No. 189, Grove St, Los Angeles",
          fee: "No. 189, Grove St, Los Angeles",
          tax: "No. 189, Grove St, Los Angeles",
          total: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          seller: "Tom",
          sku: "No. 189, Grove St, Los Angeles",
          type: "No. 189, Grove St, Los Angeles",
          status: "No. 189, Grove St, Los Angeles",
          curr: "No. 189, Grove St, Los Angeles",
          fee: "No. 189, Grove St, Los Angeles",
          tax: "No. 189, Grove St, Los Angeles",
          total: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          seller: "Tom",
          sku: "No. 189, Grove St, Los Angeles",
          type: "No. 189, Grove St, Los Angeles",
          status: "No. 189, Grove St, Los Angeles",
          curr: "No. 189, Grove St, Los Angeles",
          fee: "No. 189, Grove St, Los Angeles",
          tax: "No. 189, Grove St, Los Angeles",
          total: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          seller: "Tom",
          sku: "No. 189, Grove St, Los Angeles",
          type: "No. 189, Grove St, Los Angeles",
          status: "No. 189, Grove St, Los Angeles",
          curr: "No. 189, Grove St, Los Angeles",
          fee: "No. 189, Grove St, Los Angeles",
          tax: "No. 189, Grove St, Los Angeles",
          total: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          seller: "Tom",
          sku: "No. 189, Grove St, Los Angeles",
          type: "No. 189, Grove St, Los Angeles",
          status: "No. 189, Grove St, Los Angeles",
          curr: "No. 189, Grove St, Los Angeles",
          fee: "No. 189, Grove St, Los Angeles",
          tax: "No. 189, Grove St, Los Angeles",
          total: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          seller: "Tom",
          sku: "No. 189, Grove St, Los Angeles",
          type: "No. 189, Grove St, Los Angeles",
          status: "No. 189, Grove St, Los Angeles",
          curr: "No. 189, Grove St, Los Angeles",
          fee: "No. 189, Grove St, Los Angeles",
          tax: "No. 189, Grove St, Los Angeles",
          total: "No. 189, Grove St, Los Angeles",
        },
      ],
    });
    return { state };
  },
});
</script>

<style lang="scss">
.transaction {
  padding: 20px 30px;
  .transaction-table {
    margin-top: 20px;
    table {
      thead {
        color: #035ecf;
        font-weight: bold;
        font-size: 12px;
        text-transform: uppercase;
        font-family: "Archivo SemiExpanded", sans-serif;
      }
      .date {
        display: flex;
        gap: 20px;
        i {
          font-size: 20px;
          color: #035ecf;
        }
      }
      .seller {
        display: flex;
        gap: 20px;
        align-items: center;
        img {
          border-radius: 5px;
        }
      }
      .status {
        button {
          border: none;
          background: #035ecf;
          padding: 2px 15px;
          text-transform: uppercase;
          color: #fff;
          font-weight: bold;
          border-radius: 20px;
          font-size: 12px;
        }
      }
      .total {
        font-weight: 700;
      }
      .cell {
        padding: 24px;
      }
    }
  }
  .pagination {
    margin-top: 10px;
  }
}
</style>
