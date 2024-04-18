<template>
  <div class="reviews">
    <div class="review-card">
      <div class="review-judge">
        <div class="block">
          <el-rate v-model="value1"></el-rate>
          <div class="rate"><h5>4.5</h5></div>
          <span>Review score</span>
        </div>
      </div>
      <div class="review-judge">
        <i class="el-icon-s-custom green"></i>
        <div><h5>348</h5></div>
        <span>Total</span>
      </div>
      <div class="review-judge">
        <i class="el-icon-s-custom blue"></i>
        <div><h5>25%</h5></div>
        <span>New</span>
      </div>
      <div class="review-judge">
        <i class="el-icon-s-custom red"></i>
        <div><h5>75%</h5></div>
        <span>Regular</span>
      </div>

      <div class="reviews-progress">
        <el-progress
          :text-inside="true"
          :stroke-width="24"
          :percentage="100"
          status="success"
        ></el-progress>
        <el-progress
          :text-inside="true"
          :stroke-width="24"
          :percentage="100"
          status="success"
        ></el-progress>
        <el-progress
          :text-inside="true"
          :stroke-width="24"
          :percentage="100"
          status="success"
        ></el-progress>
        <el-progress
          :text-inside="true"
          :stroke-width="22"
          :percentage="80"
          status="warning"
        ></el-progress>
        <el-progress
          :text-inside="true"
          :stroke-width="20"
          :percentage="50"
          status="exception"
        ></el-progress>
      </div>
    </div>
    <div>
      <div class="review-latest">
        <div class="latest">
          <h5>Latest Accepted Reviews</h5>
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
        </div>
      </div>
      <div class="card">
        <div class="item">
          <img src="~assets/images/header/1.webp" width="50" />
          <div>
            <h5>Rita Amber</h5>
            <nuxt-link to="">rita@domain.com</nuxt-link>
          </div>
        </div>
        <div class="item">
          <div class="block">
            <el-rate v-model="value1"></el-rate>
          </div>
          <span>4.5</span>
        </div>
        <div class="item comment">
          <div>
            <span>Thymbra depulso denego rerum cognomen.</span>
          </div>
          <i class="el-icon-chat-dot-square"></i>
        </div>
        <div class="item column">
          <i class="el-icon-time time"></i>

          <div class="clock">
            <span class="h6">18/04/2024</span>
            <span>at 02:09 PM</span>
          </div>
        </div>
        <div class="item">
          <i class="el-icon-more rotate"></i>
        </div>
      </div>
      <div class="card">
        <div class="item">
          <img src="~assets/images/header/1.webp" width="50" />
          <div>
            <h5>Rita Amber</h5>
            <nuxt-link to="">rita@domain.com</nuxt-link>
          </div>
        </div>
        <div class="item">
          <div class="block">
            <el-rate v-model="value1"></el-rate>
          </div>
          <span>4.5</span>
        </div>
        <div class="item comment">
          <div>
            <span>Thymbra depulso denego rerum cognomen.</span>
          </div>
          <i class="el-icon-chat-dot-square"></i>
        </div>
        <div class="item column">
          <i class="el-icon-time time"></i>

          <div class="clock">
            <span class="h6">18/04/2024</span>
            <span>at 02:09 PM</span>
          </div>
        </div>
        <div class="item">
          <i class="el-icon-more rotate"></i>
        </div>
      </div>
      <div class="card">
        <div class="item">
          <img src="~assets/images/header/1.webp" width="50" />
          <div>
            <h5>Rita Amber</h5>
            <nuxt-link to="">rita@domain.com</nuxt-link>
          </div>
        </div>
        <div class="item">
          <div class="block">
            <el-rate v-model="value1"></el-rate>
          </div>
          <span>4.5</span>
        </div>
        <div class="item comment">
          <div>
            <span>Thymbra depulso denego rerum cognomen.</span>
          </div>
          <i class="el-icon-chat-dot-square"></i>
        </div>
        <div class="item column">
          <i class="el-icon-time time"></i>

          <div class="clock">
            <span class="h6">18/04/2024</span>
            <span>at 02:09 PM</span>
          </div>
        </div>
        <div class="item">
          <i class="el-icon-more rotate"></i>
        </div>
      </div>
      <div class="card">
        <div class="item">
          <img src="~assets/images/header/1.webp" width="50" />
          <div>
            <h5>Rita Amber</h5>
            <nuxt-link to="">rita@domain.com</nuxt-link>
          </div>
        </div>
        <div class="item">
          <div class="block">
            <el-rate v-model="value1"></el-rate>
          </div>
          <span>4.5</span>
        </div>
        <div class="item comment">
          <div>
            <span>Thymbra depulso denego rerum cognomen.</span>
          </div>
          <i class="el-icon-chat-dot-square"></i>
        </div>
        <div class="item column">
          <i class="el-icon-time time"></i>

          <div class="clock">
            <span class="h6">18/04/2024</span>
            <span>at 02:09 PM</span>
          </div>
        </div>
        <div class="item">
          <i class="el-icon-more rotate"></i>
        </div>
      </div>
    </div>
    <div class="pagination">
      <el-pagination background layout="prev, pager, next" :total="20"> </el-pagination>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive, ref } from "@nuxtjs/composition-api";

export default defineComponent({
  setup() {
    const value1 = ref(null);
    const state = reactive({
      options: [
        {
          value: "Option1",
          label: "Option1",
        },
        {
          value: "Option2",
          label: "Option2",
        },
        {
          value: "Option3",
          label: "Option3",
        },
        {
          value: "Option4",
          label: "Option4",
        },
      ],
      value: "",
    });
    return { value1, state };
  },
});
</script>

<style lang="scss">
.reviews {
  padding: 20px 30px;
  .review-card {
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(6, 1fr);
    .reviews-progress {
      background: #ffffff;
      padding: 20px;
      grid-column: span 2;
      display: grid;
      gap: 20px;
    }
    .review-judge {
      padding: 20px;
      background: #ffffff;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 10px;
      .green {
        padding: 10px;
        color: white;
        background: #00ba9d;
        border-radius: 5px;
      }
      .blue {
        padding: 10px;
        color: white;
        background: #035ecf;
        border-radius: 5px;
      }
      .red {
        padding: 10px;
        color: white;
        background: #ff5470;
        border-radius: 5px;
      }
      .rate {
        text-align: center;
        padding: 10px 0;
      }
      h5 {
        font-size: 25px;
        font-weight: bold;
      }
      span {
        font-size: 16px;
        font-weight: 700;
        text-align: center;
      }
    }
  }

  .review-latest {
    background: #ffffff;
    padding: 20px 30px;
    margin-top: 20px;
    .latest {
      display: flex;
      justify-content: space-between;
    }
  }
  .card {
    padding: 20px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 10px;
    .item {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      img {
        border-radius: 5px;
      }
      a {
        color: #035ecf;
      }
    }
    .comment {
      padding: 20px;
      border: 1px solid green;
      border-radius: 5px;
    }
    .time {
      font-size: 20px;
      color: #035ecf;
    }
    .clock {
      display: flex;
      flex-direction: column;
    }
    .rotate {
      transform: rotate(90deg);
      font-size: 30px;
      color: #035ecf;
    }
  }
  .pagination {
    margin-top: 20px;
  }
}
</style>
