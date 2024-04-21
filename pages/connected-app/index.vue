<template>
  <div class="connected-app">
    <div class="search">
      <div class="button">
        <button class="button-add">Add new product</button>
      </div>
      <div class="input-search">
        <el-input placeholder="Please input" class="input-with-select">
          <el-button slot="append" icon="el-icon-search"></el-button>
        </el-input>
      </div>
    </div>
    <div class="service">
      <div class="header">
        Applications : <nuxt-link class="link-header" to="">All </nuxt-link
        ><span>(20)</span>
      </div>
      <span class="line"></span>
      <div class="published">
        <nuxt-link class="link" to="">Developer Tools </nuxt-link><span>(12)</span>
      </div>
      <span class="line"></span>
      <div class="draft">
        <nuxt-link class="link" to="">Marketplace </nuxt-link><span>(15)</span>
      </div>
      <span class="line"></span>
      <div class="trash">
        <nuxt-link class="link" to="">Financial Accounting </nuxt-link><span>(11)</span>
      </div>
    </div>

    <div class="connected-app-card">
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
      <div class="card">
        <div class="card-app">
          <div class="img">
            <img src="~assets/images/seller-prolist/8.webp" width="50" />
            <h5>Tracking App</h5>
          </div>
          <el-switch v-model="value1"> </el-switch>
        </div>
        <p>Real-time order tracking and a list of bestselling products from the shops</p>
        <button class="btn-text">View settings</button>
      </div>
    </div>
    <div class="pagination">
      <el-pagination background layout="prev, pager, next" :total="20"> </el-pagination>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from "@nuxtjs/composition-api";

export default defineComponent({
  setup() {
    const value1 = ref(true);
    return {
      value1,
    };
  },
});
</script>

<style lang="scss">
.connected-app {
  padding: 20px 30px;
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
        width: 250px;
        font-weight: bold;
        box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
        transition: ease-in-out 0.3s;
        &:hover {
          background: #01c8a9;
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
  .connected-app-card {
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(4, 1fr);
    .card {
      background: #fff;
      padding: 20px;
      .card-app {
        display: flex;
        justify-content: space-between;
        background: none;
        .img {
          display: flex;
          align-items: center;
          gap: 10px;
          img {
            border: 1px solid #e2e1e1;
            border-radius: 5px;
          }
          h5 {
            font-size: 16px;
            font-weight: 700;
          }
        }
      }
      p {
        max-width: 330px;
        padding: 10px 0;
        font-size: 14px;
      }
      .btn-text {
        border: none;
        color: #035ecf;
        text-align: left;
        background: none;
        font-weight: bold;
        position: relative;

        &::after {
          content: "";
          position: absolute;
          bottom: 0;
          left: 0;
          width: 0%;
          height: 1px;
          background-color: #035ecf;
          transition: all 0.3s ease-in-out;
        }
      }
      .btn-text:hover::after {
        width: 120px;
        transition: all 0.3s ease-in-out;
      }
    }
  }
  .pagination {
    margin-top: 10px;
  }
}
</style>
