<template>
    <div class="createClub">
        <div class="clubMain">
            <div class="clubHeader">
                <div class="invite"></div>
                <h3>Club</h3>
                <div class="search"></div>
            </div>
            <div class="clubContent">
                <ul>
                    <li class="list">
                        <div class="photo"></div>
                        <div class="center">
                            <div class="context">{{ClubName}}</div>
                            <p class="des"><span>{{ID}}</span><span>{{creator}}</span></p>
                        </div>
                        <p class="deskNum">{{num}}</p>
                    </li>
                </ul>

            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "createClub",
        data() {
            return {
                num: 99,
                creator: 'Creator: I',
                ID: 'ID:18293',
                ClubName: 'Superhero Movie Club'
            }
        }
    }
</script>

<style lang="less" scoped>
    .createClub {
        position: absolute;
        top: 0;
        left: 0;
        background-color: #1C1C4B;
        width: 100%;
        height: 100%;
        .clubMain {
            width: 6.98rem;
            height: 6.02rem;
            border-radius: 0.12rem;
            text-align: center;
            background: linear-gradient(180deg, rgba(57, 94, 155, 1), rgba(38, 45, 99, 1));
            margin: 0.1rem auto 0 auto;
            .clubHeader {
                height: 1.22rem;
                box-sizing: border-box;
                line-height: 1.22rem;
                color: #CEE1FF;
                font-size: 0.42rem;
                position: relative;
                .invite {
                    width: 0.54rem;
                    height: 0.5rem;
                    background: url("../assets/images/icon_zhanqi_pre@3x.png") no-repeat center center;
                    background-size: cover;
                    position: absolute;
                    top: 0.35rem;
                    left: 0.52rem;
                }
                .search {
                    width: 0.46rem;
                    height: 0.46rem;
                    background: url("../assets/images/icon_zhanqi_pre@3x.png") no-repeat center center;
                    background-size: cover;
                    position: absolute;
                    top: 0.35rem;
                    right: 0.47rem;
                }
            }
            .clubContent {
                background: #181840;
                width: 6.71rem;
                height: 4.66rem;
                margin: 0 auto;
                border-radius: 0.12rem;
                overflow: hidden;
                .list {
                    width: 6.33rem;
                    height: 1.30rem;
                    background: linear-gradient(90deg,rgba(13,121,230,1),rgba(32,59,121,1),rgba(33,60,123,1),rgba(51,95,187,1));
                    box-shadow: 0 0 0.17rem 0 rgba(61,108,205,1);
                    border-radius: 0.08rem;
                    margin: 0.19rem auto;
                    color: #FFFFFF;
                    font-size: 0.32rem;
                    .photo {
                        width: 0.79rem;
                        height: 0.79rem;
                        border-radius: 50%;
                        background-color: #FFFFFF;
                        margin-top: 0.26rem;
                        margin-left: 0.31rem;
                        float: left;
                    }
                    .deskNum {
                        width: 0.64rem;
                        height: 0.64rem;
                        line-height: 0.64rem;
                        float: right;
                        margin-right: 0.24rem;
                        margin-top: 0.31rem;
                        background: #1E3871;
                        border-radius: 50%;
                        text-align: center;
                        color: #02C2D1;
                        font-size: 0.28rem;
                    }
                    .center {
                        float: left;
                        margin-left: 0.28rem;
                        text-align: left;
                        margin-top: 0.28rem;
                        line-height: 0.45rem;
                        .des {
                            line-height: 0.48rem;
                            font-size: 0.24rem;
                            color: #C7DAF9;
                            & > span:nth-child(1) {
                                margin-right: 0.2rem;
                            }
                            span:nth-child(2) {
                                color: #4772BD;
                                background-color: #1D2C60;
                                padding: 0 0.15rem;
                            }
                        }
                    }
                }

            }
        }
    }
</style>