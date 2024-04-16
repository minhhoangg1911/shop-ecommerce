<template>
  <div class="products-management">
    <div class="main">
      <div class="search">
        <div class="button">
          <button class="button-add">Add new product</button>
          <button class="button-export">Export CSV</button>
        </div>
        <div class="input-search">
          <el-input placeholder="Please input" class="input-with-select">
            <el-button slot="append" icon="el-icon-search"></el-button>
          </el-input>
        </div>
      </div>
      <div class="service">
        <div class="header">
          Product : <nuxt-link class="link-header" to="">All </nuxt-link
          ><span>(16)</span>
        </div>
        <span class="line"></span>
        <div class="published">
          <nuxt-link class="link" to="">Published </nuxt-link><span>(7)</span>
        </div>
        <span class="line"></span>
        <div class="draft">
          <nuxt-link class="link" to="">Drafts </nuxt-link><span>(5)</span>
        </div>
        <span class="line"></span>
        <div class="trash">
          <nuxt-link class="link" to="">Trash </nuxt-link><span>(4)</span>
        </div>
      </div>
      <div class="select">
        <div>
          <el-select v-model="state.value" placeholder="Select">
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
          <el-select v-model="state.value1" placeholder="Select">
            <el-option
              v-for="item in state.options1"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
        <div>
          <el-select v-model="state.value2" placeholder="Select">
            <el-option
              v-for="item in state.options2"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
        <div>
          <el-select v-model="state.value3" placeholder="Select">
            <el-option
              v-for="item in state.options3"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
        <div>
          <el-select v-model="state.value4" placeholder="Select">
            <el-option
              v-for="item in state.options4"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
        <div class="button">
          <button class="button-apply">Apply</button>
          <button class="button-clear">Clear</button>
        </div>
      </div>
      <div class="action">
        <div>
          <span>View products: <span class="number">8</span>/16</span>
        </div>
        <div>
          <el-select v-model="state.select" placeholder="Select">
            <el-option
              v-for="item in state.selectAction"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div>
      </div>
      <div class="table">
        <div>
          <el-table
            ref="multipleTable"
            :data="tableData"
            style="width: 100%"
            @selection-change="handleSelectionChange"
          >
            <el-table-column type="selection" width="55"> </el-table-column>
            <el-table-column label="Img" width="120">
              <img src="~assets/images/top-products/1.webp" width="50px" />
            </el-table-column>
            <el-table-column property="name" label="Name" width="120">
              <div class="name">Xiaomi WiFI Repeater Pro</div>
            </el-table-column>
            <el-table-column property="sku" label="Sku" show-overflow-tooltip>
              <div>
                <span>TR-001</span>
              </div>
            </el-table-column>
            <el-table-column property="stock" label="stock" width="120">
              <div>
                <span class="text-stock">in stock </span><span>(120)</span>
              </div>
            </el-table-column>
            <el-table-column property="price" label="price" width="120">
              <div>$110.00</div>
            </el-table-column>
            <el-table-column property="type" label="type" width="120">
              <div>Simble</div>
            </el-table-column>
            <el-table-column property="static" label="static" width="120">
              <div>Best Seller</div>
            </el-table-column>
            <el-table-column property="tags" label="tags" width="120">
              <div class="tags-button">
                <button>Top Rated,</button>
                <button>Best Seller,</button>
                <button>Phone</button>
              </div>
            </el-table-column>
            <el-table-column property="rate" label="rate" width="120">
              <i class="el-icon-star-on rate"></i> <span>(4)</span>
            </el-table-column>
            <el-table-column property="date" label="date" width="120">
              <div>Last modified:</div>
              <div class="date">11/11/2023</div>
            </el-table-column>
            <el-table-column property="actions" label="actions" width="120">
              <div class="actions-button">
                <button class="button-edit">
                  <i class="el-icon-edit-outline"></i>
                </button>
                <button class="button-menu">
                  <i class="el-icon-more"></i>
                </button>
              </div>
            </el-table-column>
          </el-table>
          <div class="pagination">
            <el-pagination background layout="prev, pager, next" :total="20">
            </el-pagination>
          </div>
          <!-- <div style="margin-top: 20px">
            <el-button @click="toggleSelection([tableData[1], tableData[2]])"
              >Chọn/Deselect hàng thứ hai và thứ ba</el-button
            >
            <el-button @click="toggleSelection()">Xóa lựa chọn</el-button>
          </div> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const tableData = ref([
      {
        img: '2016-05-03',
        name: 'Tom',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: 'Top Rated, Best Seller, Phone',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
      {
        img: '2016-05-03',
        name: 'Cu',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: 'Top Rated, Best Seller, Phone',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
      {
        img: '2016-05-03',
        name: 'Tom',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: 'Top Rated, Best Seller, Phone',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
      {
        img: '2016-05-03',
        name: 'Tom',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: 'Top Rated, Best Seller, Phone',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
      {
        img: '2016-05-03',
        name: 'Tom',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: 'Top Rated, Best Seller, Phone',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
      {
        img: '2016-05-03',
        name: 'Tom',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: 'Top Rated, Best Seller, Phone',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
      {
        img: '2016-05-03',
        name: 'Tom',
        sku: 'Tr-001',
        stock: 'in stock (120)',
        price: '$254.00',
        type: 'Simble',
        static: 'Best Seller',
        tags: '-',
        rate: '',
        date: '14/11/2023',
        actions: '',
      },
    ])
    const multipleSelection = ref([])
    const multipleTable = ref(null)
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
      value: '',
      options1: [
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
      options2: [
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
      value2: '',
      options3: [
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
      value3: '',
      options4: [
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
      value4: '',
      selectAction: [
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
      select: '',
      tableData: [],
    })
    const toggleSelection = (rows) => {
      if (rows) {
        rows.forEach((row) => {
          multipleTable.value.toggleRowSelection(row)
        })
      } else {
        multipleTable.value.clearSelection()
      }
    }
    const handleSelectionChange = (val) => {
      multipleSelection.value = val
    }

    return {
      state,
      tableData,
      multipleTable,
      toggleSelection,
      handleSelectionChange,
    }
  },
})
</script>
<style lang="scss">
.products-management {
  padding: 20px 30px;
  .main {
    .search {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .button {
        display: flex;
        gap: 20px;

        .button-add {
          padding: 10px 30px;
          border: #01c8a9;
          background: #00ba9d;
          color: #fff;
          border-radius: 25px;
          box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
          transition: ease-in-out 0.3s;
          &:hover {
            background: #01c8a9;
          }
        }
        .button-export {
          padding: 10px 30px;
          border: 1px solid #035ecf;
          color: #035ecf;
          border-radius: 25px;
          transition: ease-in-out 0.3s;
          background: #fff;
          &:hover {
            color: #fff;
            background: #035ecf;
            transition: ease-in-out 0.3s;
          }
        }
      }
      .input-search {
      }
    }
    .service {
      display: flex;
      gap: 20px;
      padding: 20px 0;

      .header {
        .link-header {
          color: #000;
          font-weight: 700;
        }
      }
      .link {
        color: #035ecf;
        font-weight: 700;
      }
      .line {
        width: 1px;
        height: 20px;
        background: #000;
      }
    }
    .select {
      display: grid;
      /* grid-template-columns: repeat(6, minmax(0,1fr)); */
      grid-template-columns: repeat(6, 1fr);
      div {
        .el-select__caret {
          color: #035ecf;
        }
        &:hover {
          border: #035ecf;
        }
      }

      .button {
        display: flex;
        gap: 20px;
        .button-apply {
          padding: 10px 35px;
          border-radius: 30px;
          border: none;
          background: #035ecf;
          color: #fff;
          transition: ease-in-out 0.3s;
          box-shadow: 0 1px 8px rgba(3, 94, 207, 0.5);
          &:hover {
            background: #2113e7;
            transition: ease-in-out 0.3s;
          }
        }
        .button-clear {
          padding: 10px 35px;
          border-radius: 30px;
          border: 1px solid #035ecf;
          color: #035ecf;
          background: #fff;
          transition: ease-in-out 0.3s;
          &:hover {
            background: #035ecf;
            color: #fff;
            transition: ease-in-out 0.3s;
          }
        }
      }
    }
    .action {
      display: flex;
      justify-content: space-between;
      padding: 20px 0;
      .el-input__inner {
        padding-right: 80px;
      }
      .number {
        color: #000;
        font-weight: 700;
      }
    }
    .table {
      .is-leaf {
        color: #035ecf;
      }
      .name {
        font-size: 14px;
        font-weight: 700;
        color: #000;
        max-width: 90px;
      }
      .text-stock {
        color: #00ba9d;
      }
      .tags-button {
        button {
          border: none;
          color: #035ecf;
          background: #fff;
          font-weight: 700;
        }
      }
      .rate {
        font-size: 20px;
        color: #035ecf;
      }
      .date {
        color: #000;
        font-weight: 700;
        font-size: 12px;
      }
      .actions-button {
        button {
          border: none;
          background: #fff;
          font-size: 20px;
          color: #035ecf;
        }
        .button-edit {
        }
        .button-menu {
          transform: rotate(90deg);
        }
      }
    }
  }
}
</style>
