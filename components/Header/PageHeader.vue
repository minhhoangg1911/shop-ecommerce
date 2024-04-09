<template>
    <header>

        <div class="page">
            <div class="left">
                <div class="left-content">
                    <i class="menu el-icon-s-unfold"></i>
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
                            <i class="el-icon-moon"></i>
                        </div>
                    </div>
                    <div class="box">
                        <div>
                            <i class="el-icon-s-custom"></i>
                        </div>
                    </div>
                    <div class="box">
                        <div>
                            <i class="el-icon-s-custom"></i>
                        </div>
                        <div class="notificate ">
                            <span class="">1</span>
                        </div>
                    </div>
                    <div class="box">
                        <div>
                            <i class="el-icon-s-custom"></i>
                        </div>
                        <div class="message ">
                            <span style="font-size: 15px ; color:white">1</span>
                        </div>
                    </div>
                    <div class="box">
                        <div>
                            <i class="el-icon-s-custom"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </header>
</template>

<style lang="scss">
@media screen and (max-width: 1000px) {

    .search {
        display: inline !important;
        font-size: 20px !important;
        color: blue
    }

    .left-input {
        display: none;
    }


}

.page {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px 0;
    gap: 10px;
    width: 100%;

    .left {
        width: 70%;

        .left-content {
            display: inline-flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            gap: 10px;
            width: 100%;

            .menu {
                font-size: 25px
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
            padding: 0 10px;
            font-size: 35px;
            position: relative;

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
        }
    }

    .input-with-select {
        position: relative;
    }

    .el-input-group__append {
        position: absolute;
        border: none;
        font-size: 15px;
        background: none;
        top: 10px;
        color: blue;
        right: 10px;
    }
}
</style>
