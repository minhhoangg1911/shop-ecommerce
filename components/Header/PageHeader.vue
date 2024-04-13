<template>
  <header>
    <div class="page">
      <div class="left">
        <div class="left-content">
          <div class="left-popup">
            <i class="menu el-icon-s-unfold" @click="drawer = true"></i>

            <el-drawer
              class="title-nav"
              title="ShopPoint"
              :visible.sync="drawer"
              :direction="direction"
              :before-close="handleClose"
            >
              <el-row class="tac">
                <el-col style="width: 100%" :span="12">
                  <el-menu
                    default-active="2"
                    class="el-menu-vertical-demo"
                    @open="handleOpenMenu"
                    @close="handleCloseMenu"
                  >
                    <el-submenu index="1">
                      <template slot="title">
                        <i class="el-icon-location"></i>
                        <span>Dashboard</span>
                      </template>
                      <el-menu-item-group>
                        <el-menu-item index="1-1">
                          <nuxt-link to="/sales-analytics"
                            >Sales Analytics</nuxt-link
                          >
                        </el-menu-item>

                        <el-menu-item index="1-2">
                          <nuxt-link to="/seller-prolist">
                            Sellers List
                          </nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="1-3">
                          <nuxt-link to="/seller-table"
                            >Sellers Table</nuxt-link
                          >
                        </el-menu-item>
                        <el-menu-item index="1-4">
                          <nuxt-link to="/seller-grid"
                            >Sellers Grid</nuxt-link
                          ></el-menu-item
                        >
                        <el-menu-item index="1-5">
                          <nuxt-link to="/seller-profile"
                            >Sellers Profile</nuxt-link
                          ></el-menu-item
                        >
                        <el-menu-item index="1-6">
                          <nuxt-link to=""
                            >Revenue by Period</nuxt-link
                          ></el-menu-item
                        >
                      </el-menu-item-group>
                    </el-submenu>
                    <el-submenu index="2">
                      <template slot="title">
                        <i class="el-icon-location"></i>
                        <span>Products</span>
                      </template>
                      <el-menu-item-group>
                        <el-menu-item index="2-1">
                          <nuxt-link to=""> Top Products</nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="2-2">
                          <nuxt-link to=""> Products Grid </nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="2-3">
                          <nuxt-link to=""> Products Management </nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="2-4">
                          <nuxt-link to="">Products Editor </nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="2-5">
                          <nuxt-link to="">Banners </nuxt-link>
                        </el-menu-item>
                      </el-menu-item-group>
                    </el-submenu>
                    <el-menu-item index="3">
                      <i class="el-icon-menu"></i>
                      <span>Orders</span>
                    </el-menu-item>
                    <el-menu-item index="4">
                      <i class="el-icon-setting"></i>
                      <span>Statistics</span>
                    </el-menu-item>
                    <el-menu-item index="5">
                      <i class="el-icon-setting"></i>
                      <span>Reviews</span>
                    </el-menu-item>
                    <el-menu-item index="6">
                      <i class="el-icon-setting"></i>
                      <span>Customers</span>
                    </el-menu-item>
                    <el-menu-item index="7">
                      <i class="el-icon-setting"></i>
                      <span>Transactions</span>
                    </el-menu-item>
                    <el-submenu index="8">
                      <template slot="title">
                        <i class="el-icon-location"></i>
                        <span>Pages</span>
                      </template>
                      <el-menu-item-group>
                        <el-menu-item index="8-1">
                          <nuxt-link to="">Login</nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="8-2">
                          <nuxt-link to="">Page 404</nuxt-link>
                        </el-menu-item>
                      </el-menu-item-group>
                    </el-submenu>
                    <el-submenu index="9">
                      <template slot="title">
                        <i class="el-icon-location"></i>
                        <span>Setting</span>
                      </template>
                      <el-menu-item-group>
                        <el-menu-item index="9-1">
                          <nuxt-link to="">General Settings</nuxt-link>
                        </el-menu-item>
                        <el-menu-item index="9-2">
                          <nuxt-link to="">Connected Apps</nuxt-link>
                        </el-menu-item>
                      </el-menu-item-group>
                    </el-submenu>
                  </el-menu>
                </el-col>
              </el-row>
            </el-drawer>
          </div>

          <!-- <i class="menu el-icon-s-unfold"></i> -->
          <div class="left-input">
            <el-input placeholder="Please input" class="input-with-select">
              <el-button slot="append" icon="el-icon-search"></el-button>
            </el-input>
          </div>
        </div>
      </div>
      <div class="right">
        <div class="right-content">
          <div class="box search">
            <div>
              <i class="el-icon-search"></i>
            </div>
          </div>
          <div class="box">
            <div>
              <i class="el-icon-sunny"></i>
              <!-- <i class="el-icon-moon"></i> -->
            </div>
          </div>
          <div class="box">
            <div>
              <el-dropdown>
                <el-button type="primary">
                  <!-- <i class="el-icon-s-custom"></i> -->
                  <img class="img" src="~assets/images/eng.webp" />
                </el-button>
                <el-dropdown-menu slot="dropdown">
                  <el-dropdown-item>
                    <img class="img-detail" src="~assets/images/de.webp" /><span
                      >(Ger)</span
                    >
                  </el-dropdown-item>
                  <el-dropdown-item>
                    <img
                      class="img-detail"
                      src="~assets/images/eng.webp"
                    /><span>(EN)</span>
                  </el-dropdown-item>
                  <el-dropdown-item>
                    <img class="img-detail" src="~assets/images/dk.webp" /><span
                      >(DK)</span
                    >
                  </el-dropdown-item>
                  <el-dropdown-item>
                    <img class="img-detail" src="~assets/images/ua.webp" /><span
                      >(UK)</span
                    >
                  </el-dropdown-item>
                </el-dropdown-menu>
              </el-dropdown>
            </div>
          </div>
          <div class="box">
            <div class="notificate-action">
              <i @click="notificate = true" class="el-icon-message-solid"></i>
              <el-drawer
                title="I am the title"
                :visible.sync="notificate"
                :with-header="false"
              >
                <div class="box-content">
                  <h3>Notifications</h3>
                  <div class="content">
                    <div class="content-info">All <span>(10)</span></div>
                    <div class="line"></div>
                    <div class="content-info">Latest <span>(3)</span></div>
                    <div class="line"></div>
                    <div class="content-info">Archive <span>(4)</span></div>
                  </div>
                  <div class="card-content">
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div>
                      <button class="btn load-more">Load More</button>
                    </div>
                  </div>
                </div>
              </el-drawer>
            </div>
            <div class="notificate">
              <span class="">1</span>
            </div>
          </div>
          <div class="box">
            <div class="message-action">
              <i @click="message = true" class="el-icon-chat-square"></i>
              <el-drawer
                title="I am the title"
                :visible.sync="message"
                :with-header="false"
              >
                <div class="box-content">
                  <h3>Messages</h3>
                  <div class="content">
                    <div class="content-info">All <span>(10)</span></div>
                    <div class="line"></div>
                    <div class="content-info">Latest <span>(3)</span></div>
                    <div class="line"></div>
                    <div class="content-info">Archive <span>(4)</span></div>
                  </div>
                  <div class="card-content">
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div class="card-detail">
                      <div class="card-img">
                        <img src="~assets/images/header/1.webp" />
                      </div>
                      <div class="card-info">
                        <h1>J. Davidson</h1>
                        <p>joned to discount program</p>

                        <div class="card-time">
                          <span>6 hours ago</span>
                          <div class="circle"></div>
                          <span>Offers</span>
                        </div>

                        <div>
                          <button class="btn btn-info blue">Accept</button>
                          <button class="btn btn-info red">Decline</button>
                        </div>
                      </div>
                    </div>
                    <div>
                      <button class="btn load-more">Load More</button>
                    </div>
                  </div>
                </div>
              </el-drawer>
            </div>
            <div class="message">
              <span style="font-size: 15px; color: white">1</span>
            </div>
          </div>
          <div class="box">
            <div class="general-settings">
              <i class="el-icon-s-custom"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { defineComponent, reactive, toRefs } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const drawers = reactive({
      drawer: false,
      direction: 'ltr',
      message: false,
      notificate: false,
    })

    const handleClose = (done) => {
      done()
    }

    const handleOpenMenu = (key, keyPath) => {
      console.log(key, keyPath)
    }
    const handleCloseMenu = (key, keyPath) => {
      console.log(key, keyPath)
    }

    return { ...toRefs(drawers), handleClose, handleOpenMenu, handleCloseMenu }
  },
})
</script>

<style lang="scss">
@media screen and (max-width: 1285px) {
  .search {
    display: inline !important;
    font-size: 20px !important;
    color: blue;
  }

  .left-input {
    display: none;
  }
}

a {
  text-decoration: none;
  color: #6e757f;
}

.img-detail {
  width: 30px;
  height: 30px;
  border-radius: 50px;
}

.page {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px 0;
  gap: 10px;
  width: 100%;

  .title-nav {
    color: black;
    font-size: 30px;
    font-weight: bold;
  }

  .left {
    width: 70%;

    .left-content {
      display: inline-flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;
      gap: 10px;
      width: 100%;
      position: relative;

      .menu {
        font-size: 25px;
      }

      .left-input {
        width: 100%;
      }
    }
  }

  .right {
    width: 30%;
  }

  .right-content {
    display: inline-flex;
    justify-content: flex-end;
    align-items: center;
    padding: 0 20px;
    gap: 10px;
    width: 100%;

    .search {
      display: none;
    }

    .box {
      padding: 0 5px;
      font-size: 25px;
      position: relative;

      .general-settings {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 50px;
        width: 50px;
        font-size: 25px;
        background: blue;
        color: white;
        border-radius: 50px;
      }

      .img {
        width: 30px;
        height: 30px;
        border-radius: 50px;
      }

      .el-button {
        background: none;
        border: none;
      }

      .notificate {
        width: 20px;
        height: 20px;
        background: rgb(245, 6, 6);
        border-radius: 50px;
        position: absolute;
        top: 0;
        right: 0;

        span {
          position: absolute;
          font-size: 15px;
          color: white;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }
      }

      .message {
        width: 20px;
        height: 20px;
        background: rgb(3, 244, 23);
        border-radius: 50px;
        position: absolute;
        top: 0;
        right: 0;

        span {
          position: absolute;
          font-size: 15px;
          color: white;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }
      }

      .box-content {
        padding: 20px 40px;

        .content {
          display: flex;
          gap: 10px;
          font-size: 15px;
          font-weight: bold;

          .line {
            line-height: 15px;
            width: 2px;
            background: black;
          }

          span {
            opacity: 0.5;
          }
        }

        .card-content {
          margin-top: 20px;

          .card-detail {
            display: flex;
            gap: 10px;

            .card-img {
              width: 40px;

              img {
                width: 40px;
                border-radius: 5px;
              }
            }

            .card-info {
              padding: 10px 0;

              h1 {
                font-size: 15px;
                font-weight: bold;
              }

              p {
                display: inline;
                font-size: 15px;
                color: #515c6b;
              }

              span {
                font-size: 12px;
                color: #515c6b;
                opacity: 0.7;
              }

              .card-time {
                display: flex;
                align-items: center;
                gap: 5px;
                margin-bottom: 5px;

                .circle {
                  width: 5px;
                  height: 5px;
                  background: #515c6b;
                  border-radius: 50px;
                  opacity: 0.7;
                }
              }

              .btn-info {
                background: none;
                font-size: 10px;
                font-weight: bold;
                border-radius: 20px;
                padding: 5px 15px;
              }

              .red {
                border: 1px solid red;
                color: red;

                &:hover {
                  background: red;
                  color: #fff;
                  border: none;
                }
              }

              .blue {
                border: 1px solid blue;
                color: blue;

                &:hover {
                  background: blue;
                  color: #fff;
                  border: none;
                }
              }
            }
          }
        }
      }

      .load-more {
        border: none;
        background: blue;
        color: white;
        width: 100%;
        padding: 10px 15px;
        border-radius: 20px;
        box-shadow: 0 1px 8px rgba(3, 94, 207, 0.5);

        &:hover {
          background: rgb(91, 91, 218);
        }
      }
    }
  }
}
</style>
