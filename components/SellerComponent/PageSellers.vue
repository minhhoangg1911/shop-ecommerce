<template>
    <div class="sellers">
        <div class="content">
            <div class="title">
                <h1>Sales Analytics</h1>
            </div>
            <div class="Refresh">
                <div class="Refresh-detail">
                    <div>Data Refresh</div>
                    <i class="el-icon-refresh"></i>
                </div>
                <div class="time">
                    April 11, 2024 15:10 PM
                </div>
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.sellers {
    padding: 20px 30px;

    .content {
        padding: 20px 30px;
        background: #FFFFFF;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .title {
            h1 {
                font-weight: bold;
                font-size: 40px;
            }
        }

        .Refresh {
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            gap: 10px;

            .Refresh-detail {
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 10px;
            }

            .time {
                padding: 10px 40px;
                background: #F9F9F9;
                font-weight: bold;
            }
        }
    }
}
</style>