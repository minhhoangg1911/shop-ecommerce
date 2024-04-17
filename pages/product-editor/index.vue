<template>
  <div class="product-editor">
    <div class="main">
      <div class="card">
        <h5>Product Settings</h5>
        <form action="">
          <div>
            <div>
              <span class="title">Product-images</span>
              <div class="product-upload">
                <div class="presentation">
                  <el-upload
                    class="avatar-uploader"
                    action="https://jsonplaceholder.typicode.com/posts/"
                    :show-file-list="false"
                    :on-success="handleAvatarSuccess"
                    :before-upload="beforeAvatarUpload"
                  >
                    <img v-if="imageUrl" :src="imageUrl" class="avatar" />
                    <i v-else class="el-icon-plus avatar-uploader-icon"></i>
                  </el-upload>
                </div>
                <div class="presentation">
                  <el-upload
                    class="avatar-uploader"
                    action="https://jsonplaceholder.typicode.com/posts/"
                    :show-file-list="false"
                    :on-success="handleAvatarSuccess"
                    :before-upload="beforeAvatarUpload"
                  >
                    <img v-if="imageUrl" :src="imageUrl" class="avatar" />
                    <i v-else class="el-icon-plus avatar-uploader-icon"></i>
                  </el-upload>
                </div>
                <div class="two-presentation">
                  <el-upload
                    class="avatar-uploader"
                    action="https://jsonplaceholder.typicode.com/posts/"
                    :show-file-list="false"
                    :on-success="handleAvatarSuccess"
                    :before-upload="beforeAvatarUpload"
                  >
                    <img v-if="imageUrl" :src="imageUrl" class="avatar" />
                    <i v-else class="el-icon-plus avatar-uploader-icon"></i>
                  </el-upload>
                  <el-upload
                    class="avatar-uploader"
                    action="https://jsonplaceholder.typicode.com/posts/"
                    :show-file-list="false"
                    :on-success="handleAvatarSuccess"
                    :before-upload="beforeAvatarUpload"
                  >
                    <img v-if="imageUrl" :src="imageUrl" class="avatar" />
                    <i v-else class="el-icon-plus avatar-uploader-icon"></i>
                  </el-upload>
                </div>
              </div>
            </div>
            <div>
              <button class="text-btn mt-4 mb-2.5">More Gallery Options</button>
              <p>
                Donec luctus metus nec enim imperdiet, in dignissim risus
                fringilla. Fusce bibendum vulputate scelerisque. Donec in nunc
                quam. Suspendisse at lorem eleifend
              </p>
              <button class="text-btn mt-3 mb-6">
                Attachment files
                <i class="icon-paperclip-vertical-regular text-16"></i>
              </button>
            </div>
            <div class="product-calculator">
              <div class="product-card">
                <div class="field-wrapper">
                  <label class="field-label">Attributes</label>
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
                <div class="field-wrapper">
                  <label class="field-label">L * W * H, inches</label>
                  <input class="field-input" />
                </div>
                <div class="field-wrapper">
                  <label class="field-label">Weight, kg</label>
                  <input class="field-input" />
                </div>
              </div>
              <div class="field-wrapper">
                <label class="field-label">Description</label>
                <textarea class="field-input"></textarea>
              </div>
            </div>
          </div>
          <div class="product-form">
            <div class="field-wrapper">
              <label class="field-label">Product Name</label>
              <input class="field-input" />
            </div>
            <div class="field-item select">
              <div class="field-wrapper">
                <label class="field-label">Brand Name</label>
                <input class="field-input" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Category</label>
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
            <div class="field-item">
              <div class="field-wrapper">
                <label class="field-label">Regular Price</label>
                <input class="field-input" />
              </div>
              <div class="field-wrapper">
                <label class="field-label">Sale Price</label>
                <input class="field-input" />
              </div>
            </div>

            <div class="field-item select">
              <div class="field-wrapper">
                <label class="field-label">Schedule</label>

                <div>
                  <el-date-picker
                    v-model="values"
                    type="daterange"
                    range-separator="-"
                    start-placeholder="Start date"
                    end-placeholder="End date"
                    :default-time="['00:00:00', '23:59:59']"
                  >
                  </el-date-picker>
                </div>
              </div>
              <div class="field-wrapper">
                <label class="field-label">Promotion</label>
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
            <div class="field-item select">
              <div class="field-wrapper">
                <label class="field-label">Product Type</label>

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
              <div class="field-wrapper">
                <label class="field-label">Stock Status</label>
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
            <div class="field-wrapper">
              <label class="field-label">Sku</label>
              <input class="field-input" />
            </div>
            <div class="field-item selects">
              <div class="field-wrapper">
                <label class="field-label">Stock Status</label>

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
              <div class="field-double">
                <div class="field-wrapper">
                  <label class="field-label">Quantity in Stock</label>
                  <input class="field-input" />
                </div>
                <div class="field-wrapper">
                  <label class="field-label">Unit</label>
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
            </div>
            <div class="field-wrapper">
              <span class="field-label">Payment Methods</span>
              <div class="field-checkbox">
                <el-checkbox-group v-model="checkList">
                  <el-checkbox label="Option A">
                    <img
                      src="~assets/images/product-editor/visa.svg"
                      width="50px"
                    />
                  </el-checkbox>
                  <el-checkbox label="Option B">
                    <img
                      src="~assets/images/product-editor/visa.svg"
                      width="50px"
                    />
                  </el-checkbox>
                  <el-checkbox label="Option C">
                    <img
                      src="~assets/images/product-editor/visa.svg"
                      width="50px"
                    />
                  </el-checkbox>
                  <el-checkbox label="Option D">
                    <img
                      src="~assets/images/product-editor/visa.svg"
                      width="50px"
                    />
                  </el-checkbox>
                  <el-checkbox label="Option E">
                    <img
                      src="~assets/images/product-editor/visa.svg"
                      width="50px"
                    />
                  </el-checkbox>
                </el-checkbox-group>
                <button><i class="el-icon-plus"></i></button>
              </div>
            </div>
            <div class="button">
              <button class="btn-draft">Save to Drafts</button>
              <button class="btn-publish">Publish Product</button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, reactive, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const imageUrl = ref('')
    const values = ref('')
    const checkList = ref(['selected'])
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
    })

    const handleAvatarSuccess = (res, file) => {
      imageUrl.value = URL.createObjectURL(file.raw)
    }

    const beforeAvatarUpload = (file) => {
      const isJPG = file.type === 'image/jpeg'
      const isLt2M = file.size / 1024 / 1024 < 2

      if (!isJPG) {
        this.$message.error('Hình đại diện phải có định dạng JPG!')
      }
      if (!isLt2M) {
        this.$message.error('Kích thước hình đại diện không được vượt quá 2MB!')
      }
      return isJPG && isLt2M
    }

    return {
      imageUrl,
      handleAvatarSuccess,
      beforeAvatarUpload,
      state,
      values,
      checkList,
    }
  },
})
</script>

<style lang="scss">
.product-editor {
  padding: 20px 30px;
  .main {
    flex-grow: 1;
    margin: 26px 0 22px;
    display: flex;
    flex-direction: column;
    box-shadow: 0px 3px 14px rgba(226, 225, 225, 0.75);
    .card {
      padding: 20px 30px;
    }
    .title {
      display: inline-block;
      padding: 20px 0;
    }
    form {
      display: grid;
      gap: 2.5rem;
      grid-template-columns: minmax(0, 1fr) minmax(0, 550px);

      .product-upload {
        display: grid;
        gap: 20px;

        grid-template-columns: repeat(5, minmax(0, 1fr));
        .presentation {
          border: 1px dashed #e2e1e1;
          height: 100%;
          display: grid;
          grid-column: span 2 / span 2;
          background: #f9f9f9;
        }
        .two-presentation {
          height: 100%;
          display: grid;
          gap: 20px;
          grid-template-columns: repeat(1, minmax(0, 1fr));
          background: #f9f9f9;
        }
      }
      .product-calculator {
        display: flex;
        flex-direction: column;
        .product-card {
          display: grid;
          gap: 20px;
          padding: 20px 0;
          grid-template-columns: minmax(0, 1fr) minmax(0, 1fr) minmax(0, 205px);
        }

        .field-wrapper {
          display: flex;
          flex-direction: column;
          gap: 10px;
        }
        .field-item {
          display: grid;
          grid-template-columns: repeat(2, minmax(0, 1fr));
          column-gap: 0.5rem;
          row-gap: 1rem;
        }
        .field-label {
          font-weight: 700;
          font-size: 12px;
          color: #8d8d99;
          width: fit-content;
        }
        .field-input {
          padding: 5px 10px;
          border: 1px solid #e2e1e1;
          input {
            padding: 20px;
          }
        }
        .el-select {
          width: 100%;
        }
      }
      .text-btn {
        font-family: 'Archivo SemiExpanded', sans-serif;
        font-weight: 600;
        font-size: 14px;
        line-height: 1;
        color: #035ecf;
        position: relative;
        border: none;
        background: #f9f9f9;
        width: fit-content;
        display: inline-flex;
        align-items: center;
        gap: 4px;
      }

      .product-form {
        padding: 30px 0px;
        display: grid;
        row-gap: 1rem;
        column-gap: 0.5rem;
        grid-template-columns: repeat(1, minmax(0, 1fr));
        .selects {
          display: grid;
          grid-template-columns: repeat(2, minmax(0, 1fr));
          .field-double {
            display: grid;
            gap: 10px;
            grid-template-columns: minmax(0, 1fr) minmax(0, 112px);
          }
        }
        .field-wrapper {
          display: flex;
          flex-direction: column;
          gap: 10px;
        }
        .field-item {
          display: grid;
          grid-template-columns: repeat(2, minmax(0, 1fr));
          column-gap: 0.5rem;
          row-gap: 1rem;
        }
        .field-label {
          font-weight: 700;
          font-size: 12px;
          color: #8d8d99;
          width: fit-content;
        }
        .field-input {
          padding: 5px 10px;
          border: 1px solid #e2e1e1;
        }
        .field-checkbox {
          display: flex;
          gap: 1.25rem;
          flex-wrap: wrap;
          button {
            border: #f1f1f1;
            border-radius: 6px;
          }
        }
        .button {
          display: grid;
          /* grid-template-columns: repeat(2, 1fr); */
          gap: 0.5rem;
          gap: 0.5rem;
          grid-template-columns: repeat(2, minmax(0, 1fr));
          margin-top: 20px;
          button {
            height: 44px;
            border-radius: 23px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 16px;
            line-height: 1;
            font-size: 16px;
            font-family: 'Archivo SemiExpanded', sans-serif;
            font-weight: 600;
            padding: 0 26px;
            transition: 0.3s ease-in-out;
            cursor: pointer;
          }
          .btn-draft {
            background-color: #035ecf;
            border: 1px solid #035ecf;
            color: #fff;
            box-shadow: 0 1px 8px rgba(3, 94, 207, 0.5);
            &:hover {
              background: #2012e5;
            }
          }
          .btn-publish {
            background-color: #00ba9d;
            border: 1px solid #01c8a9;
            color: #fff;
            box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
            &:hover {
              background: #59e8d3;
            }
          }
        }

        .el-checkbox {
          position: relative;
        }
        .el-checkbox__input {
          position: absolute;
          top: 30px;
          left: 30px;
        }
        .el-checkbox__inner {
          border-radius: 50px;
        }
        .el-select {
          width: 100%;
        }

        .el-input__inner {
          width: 100%;
        }
      }
      .avatar-uploader {
        display: flex;
        justify-content: center;
        align-items: center;
      }

      .avatar-uploader .el-upload {
        border: 1px dashed #d9d9d9;
        border-radius: 6px;
        cursor: pointer;
        position: relative;
        overflow: hidden;
      }
      .avatar-uploader .el-upload:hover {
        border-color: #409eff;
      }
      .avatar-uploader-icon {
        font-size: 28px;
        color: #8c939d;
        width: 178px;
        height: 178px;
        line-height: 178px;
        text-align: center;
      }
      .avatar {
        width: 178px;
        height: 178px;
        display: block;
      }
    }
  }
}
</style>
