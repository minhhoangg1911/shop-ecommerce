<template>
  <div class="top-products">
    <div class="products">
      <div class="seller-rating">
        <div class="seller-title">Top Sales by Category:</div>
        <div class="rating">
          <div class="rating-chart">
            <div class="rating-service">
              <div class="rating-title">Electronics</div>
              <span>$6.34k</span>
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
              <div class="rating-title">Fashion</div>
              <span>$2.52k</span>
            </div>
            <el-progress
              :text-inside="true"
              :stroke-width="24"
              :percentage="20"
              status="success"
            ></el-progress>
          </div>
        </div>
        <div class="rating">
          <div class="rating-chart">
            <div class="rating-service">
              <div class="rating-title">Food & Drinks</div>
              <span>$12.10k</span>
            </div>
            <el-progress
              :text-inside="true"
              :stroke-width="22"
              :percentage="50"
              status="warning"
            ></el-progress>
          </div>
        </div>
        <div class="rating">
          <div class="rating-chart">
            <div class="rating-service">
              <div class="rating-title">Services</div>
              <span>$5.00k</span>
            </div>
            <el-progress
              :text-inside="true"
              :stroke-width="20"
              :percentage="25"
              status="exception"
            ></el-progress>
          </div>
        </div>
      </div>

      <div class="products-card">
        <div class="card-body">
          <img src="~assets/images/seller-grid/4.webp" />
        </div>
        <div class="card-footer">
          <i class="el-icon-monitor electronic"></i>

          <div class="card-service">
            <span class="label-text">Electronics</span>
            <span class="h5">$256k</span>
          </div>
        </div>
      </div>
      <div class="products-card">
        <div class="card-body">
          <img src="~assets/images/seller-grid/4.webp" />
        </div>
        <div class="card-footer">
          <i class="el-icon-milk-tea food"></i>

          <div class="card-service">
            <span class="label-text">Groceries</span>
            <span class="h5">$101k</span>
          </div>
        </div>
      </div>
      <div class="products-card">
        <div class="card-body">
          <img src="~assets/images/seller-grid/4.webp" />
        </div>
        <div class="card-footer">
          <i class="el-icon-s-shop fashion"></i>

          <div class="card-service">
            <span class="label-text">Fashion</span>
            <span class="h5">$41k</span>
          </div>
        </div>
      </div>
      <div class="products-card">
        <div class="card-body">
          <img src="~assets/images/seller-grid/4.webp" />
        </div>
        <div class="card-footer">
          <i class="el-icon-monitor service"></i>

          <div class="card-service">
            <span class="label-text">Services</span>
            <span class="h5">$100k</span>
          </div>
        </div>
      </div>
    </div>
    <div class="products-carousel">
      <el-row>
        <el-col :span="12">
          <div class="carousel-content">
            <div class="carousel-icon">
              <i class="el-icon-monitor electronic"></i>
              <span>Electronics</span>
            </div>
            <div class="carousel-card">
              <VueSlickCarousel
                v-bind="state.settings"
                center-padding="50px"
                :dots="true"
              >
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
              </VueSlickCarousel>
            </div>
          </div>
        </el-col>
        <el-col :span="12">
          <div class="carousel-content">
            <div class="carousel-icon">
              <i class="el-icon-monitor fashion"></i>
              <span>Fashion</span>
            </div>
            <div class="carousel-card">
              <VueSlickCarousel
                v-bind="state.settings"
                :arrows="true"
                :dots="true"
              >
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
              </VueSlickCarousel>
            </div>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="12">
          <div class="carousel-content">
            <div class="carousel-icon">
              <i class="el-icon-monitor food"></i>
              <span>Groceries</span>
            </div>
            <div class="carousel-card">
              <VueSlickCarousel
                v-bind="state.settings"
                center-padding="50px"
                :dots="true"
              >
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
              </VueSlickCarousel>
            </div>
          </div>
        </el-col>
        <el-col :span="12">
          <div class="carousel-content">
            <div class="carousel-icon">
              <i class="el-icon-monitor service"></i>
              <span>Services</span>
            </div>
            <div class="carousel-card">
              <VueSlickCarousel
                v-bind="state.settings"
                :arrows="true"
                :dots="true"
              >
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
                <div class="card-detail">
                  <div class="card-content">
                    <div class="card-img">
                      <img src="~assets/images/top-products/1.webp" />
                      <div>
                        <i class="el-icon-more rotate"></i>
                      </div>
                    </div>
                    <div class="card-title">
                      <nuxt-link to="">
                        Oculus Quest 2 VR Headset 64 GP
                      </nuxt-link>
                    </div>
                    <div class="card-judge">
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                      <i class="el-icon-star-on"></i>
                    </div>
                    <p class="text-available">Available : 1006</p>
                    <p class="text-sold">Already sold : 19874</p>
                  </div>
                </div>
              </VueSlickCarousel>
            </div>
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive } from '@nuxtjs/composition-api'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default defineComponent({
  components: {
    VueSlickCarousel,
  },
  setup() {
    const state = reactive({
      settings: {
        dots: true,
        // dotsClass: 'slick-dots custom-dot-class',
        edgeFriction: 0.35,
        infinite: false,
        speed: 500,
        slidesToShow: 3,
        slidesToScroll: 1,
      },
    })
    return { state }
  },
})
</script>

<style lang="scss" >
.top-products {
  .el-row {
    margin-top: 50px;
  }
  .slick-dots li button:before {
    margin-top: 20px;
    font-size: 10px;
    color: #035ecf;
  }
  .products {
    display: flex;
    justify-content: space-between;
    padding: 20px 30px;

    .seller-rating {
      padding: 20px 30px;
      background: #ffffff;
      box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
      .seller-title {
        font-size: 25px;
        font-weight: bold;
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
    }
    .products-card {
      background: #ffffff;
      box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
      padding: 20px 30px;
      .card-body {
        padding: 0 20px;
        border: 1px solid #f1f1f1;
        border-radius: 5px;
      }
      .card-footer {
        display: flex;
        gap: 30px;
        align-items: center;
        margin-top: 20px;
        i {
          padding: 10px;
          background: #035ecf;
          color: #fff;
          border-radius: 5px;
        }
        .electronic {
          background: #035ecf;
        }
        .food {
          background: #00193b;
        }
        .fashion {
          background: #ff5470;
        }
        .service {
          background: #f8d518;
        }
        .card-service {
          display: flex;
          flex-direction: column;
          .label-text {
            font-size: 14px;
            font-weight: 700;
            color: #6e757f;
          }
          .h5 {
            font-weight: 700;
            line-height: 1.1;
            color: #00193b;
          }
        }
      }
    }
  }

  .products-carousel {
    padding: 20px 30px;
    .slick-slide {
      width: 225px !important;
      margin: 0 9px;
    }
    .carousel-content {
      .carousel-icon {
        padding: 0 10px;
        display: flex;
        gap: 20px;
        margin-bottom: 20px;
        i {
          padding: 10px;
          color: white;
          background: #035ecf;
          border-radius: 5px;
        }
        .fashion {
          background: #ff5470;
        }
        .food {
          background: #00193b;
        }
        .service {
          background: #f8d518;
        }
        span {
          color: black;
          font-size: 20px;
          font-weight: bold;
        }
      }
    }
    .card-detail {
      display: flex;
      align-items: center;
      padding: 20px 10px;
      background: #fff;

      .card-content {
        background: #ffffff;
        padding: 20px;

        .card-img {
          display: flex;
          background: #ffffff;
          gap: 20px;

          img {
            width: 150px;
            border: 1px solid #f1f1f1;
            background: #ffffff;
            padding: 0 20px;
          }
          .rotate {
            transform: rotate(90deg);
            color: #035ecf;
            font-size: 20px;
            font-weight: bold;
          }
        }
        .card-title {
          margin-top: 5px;
          padding: 0 20px;
          font-size: 14px;
          color: black;
          font-weight: bold;
          max-width: 200px;
          a {
            color: black;
          }
        }
        .card-judge {
          padding: 0 20px;
          font-size: 20px;
          color: yellow;
        }
        .text-available {
          padding: 0 20px;
          color: #00ba9d;
        }
        .text-sold {
          padding: 0 20px;
          color: #035ecf;
        }
      }
    }
  }
}
</style>
