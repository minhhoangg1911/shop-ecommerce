<template>
  <div class="general-setting">
    <div class="user">
      <div class="user-info">
        <div class="user-img">
          <img src="~assets/images/header/1.webp" width="100" />
          <div><i class="el-icon-camera-solid"></i></div>
        </div>
        <h5>Maria Smith</h5>
        <span class="account">Admin</span>
        <p class="visit">last visit 21/04/2024</p>
        <button>Log Out</button>
      </div>
      <div class="user-notification">
        <div class="notification">
          <i class="el-icon-message-solid"></i>
          <span>Notifications <span class="title"> (2)</span></span>
        </div>
        <div class="message">
          <i class="el-icon-chat-square"></i>
          <span>Message <span class="title">(7)</span></span>
        </div>
      </div>
      <div class="user-address">
        <div class="">
          <i class="el-icon-message"></i>
          <span>maria@gmail.com</span>
        </div>
        <div class="">
          <i class="el-icon-message"></i>
          <span>312 3rd St, Albany, New York 12206, USA</span>
        </div>
        <div class="">
          <i class="el-icon-message"></i>
          <span>+1 123-123-123</span>
        </div>
        <div class="">
          <i class="el-icon-message"></i>
          <span>+1 123-123-123</span>
        </div>
        <div class="">
          <i class="el-icon-message"></i>
          <span>Profile Information file</span>
        </div>
      </div>
    </div>
    <div class="user-form">
      <div class="form">
        <div>
          <h5>My profile Details</h5>
        </div>
        <form>
          <div class="form-grid">
            <div class="form-content">
              <div class="field-wrapper">
                <label class="field-label">First Name</label>
                <input class="field-input" placeholder="Maria" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Last Name</label>
                <input class="field-input" placeholder="Smith" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Email</label>
                <input class="field-input" placeholder="maria@email.com" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Phone Number</label>
                <input class="field-input" placeholder="Smith" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Password</label>
                <input class="field-input" placeholder="Smith" />
                <div class="icon">
                  <i class="el-icon-view"></i>
                </div>
              </div>
            </div>
            <div class="form-content">
              <div class="field-wrapper">
                <label class="field-label">Country</label>

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
              <div class="field-wrapper">
                <label class="field-label">City</label>

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
              <div class="field-wrapper">
                <label class="field-label">State</label>
                <input class="field-input" placeholder="State" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Zip Code</label>
                <input class="field-input" placeholder="Zip Code" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Address</label>
                <input class="field-input" placeholder="Address" />
              </div>
            </div>
          </div>
          <div class="button">
            <button class="btn-change">Change password</button>
            <button class="btn-update">Update information</button>
          </div>
        </form>

        <div class="admin-tool">
          <div>
            <h5>Admin Panel Tools</h5>
          </div>
          <div class="admin-icon">
            <div>
              <i class="el-icon-s-operation"></i>
              <span>Connected App <span class="title">(12)</span></span>
            </div>
            <div>
              <i class="el-icon-s-operation"></i>
              <span>Payment Methods</span>
            </div>
            <div>
              <i class="el-icon-s-operation"></i>
              <span>Appearance</span>
            </div>
            <div>
              <i class="el-icon-s-operation"></i>
              <span>Security Assets</span>
            </div>
            <div>
              <i class="el-icon-s-operation"></i>
              <span>Configuration Settings</span>
            </div>
            <div>
              <i class="el-icon-s-operation"></i>
              <span>View Mode</span>
            </div>
           
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
        {
          value: "Option5",
          label: "Option5",
        },
      ],
      value: "",
    });
    return {
      state,
    };
  },
});
</script>

<style lang="scss">
.general-setting {
  padding: 20px 30px;
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(4, 1fr);
  .user {
    text-align: center;
    display: grid;
    grid-column: span 1 / span 1;

    gap: 30px;
    .user-info {
      background: #fff;
      padding: 30px;
      .user-img {
        position: relative;
        img {
          border-radius: 50px;
        }
        i {
          position: absolute;
          bottom: 0;
          right: 90px;
          font-size: 20px;
          color: #fff;
          padding: 5px;
          background: #00ba9d;
          border: 2px solid #fff;
          border-radius: 50px;
        }
      }
      h5 {
        font-size: 20px;
        font-weight: bold;
        padding: 5px 0;
      }
      .account {
        padding: 5px 20px;
        background: #ff5470;
        font-size: 14px;
        color: white;
        border-radius: 5px;
      }
      .visit {
        margin-top: 10px;
        color: #035ecf;
        /* color: rgb(3 94 207 / 50%); */
      }
      button {
        background: #035ecf;
        box-shadow: 0 1px 8px rgba(3, 94, 207, 0.5);
        color: white;
        padding: 5px 20px;
        border: none;
        border-radius: 20px;
        width: 100%;
        font-size: 18px;
        font-weight: bold;
      }
    }
    .user-notification {
      background: #fff;
      padding: 20px;
      .notification {
        display: flex;
        align-items: center;
        gap: 20px;
        padding: 10px 0;
        i {
          font-size: 20px;
          color: #ff5470;
        }
        .title {
          color: #035ecf;
          font-weight: bold;
        }
      }
      .message {
        display: flex;
        align-items: center;
        gap: 20px;
        padding: 10px 0;
        i {
          font-size: 20px;
          color: #00ba9d;
        }
        .title {
          color: #035ecf;
          font-weight: bold;
        }
      }
    }
    .user-address {
      background: #fff;
      padding: 20px;
      div {
        display: flex;
        align-items: center;
        gap: 20px;
        padding: 10px 0;
        i {
          color: #035ecf;
          font-size: 20px;
        }
        span {
          max-width: 156px;
        }
      }
    }
  }
  .user-form {
    display: grid;
    grid-column: span 3 / span 3;

    .form {
      background: #fff;
      padding: 20px;
      h5 {
        font-weight: bold;
      }
      .form-grid {
        display: grid;
        gap: 20px;
        grid-template-columns: repeat(2, 1fr);
        .field-wrapper {
          display: flex;
          flex-direction: column;
          position: relative;
          .el-input__inner {
            height: 45px;
          }
        }
        .field-label {
          padding: 10px 0;
          font-weight: 700;
          font-size: 12px;
          color: #8d8d99;
          width: fit-content;
        }
        .field-input {
          padding: 10px 10px;
          border: 1px solid #e2e1e1;
          border-radius: 5px;
          position: relative;
        }
        .icon {
          position: absolute;
          bottom: 10px;
          right: 15px;
          color: #035ecf;
          font-size: 18px;
          cursor: pointer;
        }
      }
      .button {
        margin-top: 10px;
        display: flex;
        flex-direction: column;
        .btn-change {
          width: 200px;
          border: none;
          background: none;
          text-align: left;
          color: #035ecf;
          font-weight: 600;
        }
        .btn-update {
          margin-top: 20px;
          width: 300px;
          padding: 10px 20px;
          background: #00ba9d;
          border: none;
          color: #fff;
          font-weight: bold;
          border-radius: 20px;
          box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
        }
      }
      .admin-tool {
        margin-top: 20px;
        .admin-icon {
            display: grid;
            gap: 20px;
            grid-template-columns: repeat(3, 1fr);
            div {
                display: flex;
                align-items: center;
                gap: 20px;
                padding: 15px 0;
                i {
                    color: #035ecf;
                    font-size: 20px;
                }
                span {
                    color: #000;
                    font-size: 16px;
                    font-weight: 500;
                }
                .title {
                    color: #035ecf;
                }
            }
        }
      }
    }
  }
}
</style>
