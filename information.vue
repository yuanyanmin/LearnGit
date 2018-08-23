<template>
    <div class="information" v-show="isShow">
        <div class="infoPrompt">
            <h3>Notice</h3>
            <a href="javascript:;"><span class="close-x" @click="close"></span></a>
            <div class="infoContext">
                <p>{{info}}</p>
            </div>

        </div>
    </div>
    <!--<Club></Club>-->
</template>

<script>
    export default {
        name: "information",
        data() {
            return {
                info: 'The club does not exist.',
                isShow: true,
            }
        },
        methods: {
            close() {
                this.isShow = false;
            }
        }
    }
</script>

<style lang="less" scoped>
    .information {
        position: absolute;
        top: 0;
        left: 0;
        background-color: rgba(0,0,0,0.75);
        height: 100%;
        width: 100%;
        .infoPrompt {
            width: 6.97rem;
            height: 4.38rem;
            background:linear-gradient(180deg,rgba(57,94,155,1),rgba(38,45,99,1));
            position: absolute;
            top: 50%;
            left: 50%;
            margin-left: -3.48rem;
            margin-top: -2.19rem;
            border-radius: 0.12rem;
            color: #000000;
            font-size: 0.4rem;
            text-align: center;
            border: 0.01rem solid #3C458D;
            h3 {
                height: 1.25rem;
                box-sizing: border-box;
                line-height: 1.25rem;
                color: #CEE1FF;
                font-size: 0.42rem;
            }
            .close-x {
                width: 0.55rem;
                height: 0.55rem;
                border-radius: 0.12rem;
                position: absolute;
                top: 0.31rem;
                right: 0.17rem;
                text-align: center;
                background-color: rgba(26, 45, 78, 0.32);
                border: 0.02rem solid rgba(24, 24, 64, 0.32);
                line-height: 0.55rem;
            }
            .infoContext {
                width: 6.71rem;
                height: 2.99rem;
                background-color: #181840;
                margin: 0 auto;
                p {
                    margin-right: 0.54rem;
                    font-size: 0.38rem;
                    color: #E5E9E7;
                    padding-top: 0.67rem;
                }
            }

        }
    }
</style>