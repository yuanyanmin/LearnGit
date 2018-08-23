<template>
    <div class="clubName">
        <ul class="clubList">
           <li>
               <div class="photo"></div>
               <div class="center">
                   <div>
                       <span>Room 107<b></b></span>
                       <em>Status 2/5</em>
                   </div>
                   <div>
                       <i> Blind 0.025/0.025 </i>
                       <em>01:32:46</em>
                   </div>
               </div>

           </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "clubName",
        data() {
            return {
                ClubRoom: 'Room 107',
            }
        }
    }
</script>

<style lang="less" scoped>
    .clubList{
        li {
            width: 7.22rem;
            height: 1.3rem;
            background: linear-gradient(90deg,rgba(14,205,172,1),rgba(34,137,117,1),rgba(32,134,114,1),rgba(10,219,178,1));
            box-shadow: 0rem 0rem 0.17rem 0rem rgba(0,255,211,1);
            border-radius: 0.08rem;
            margin: 0.24rem auto 0.17rem auto;

            position: relative;

            &:after {
                position: absolute;
                content: '';
                display: block;
                top: 50%;
                right: 0.25rem;
                margin-top: -0.27rem;
                height: 0.54rem;
                width: 0.54rem;
                background: #134D42;
                border-radius: 100%;
            }
            &:before {
                position: absolute;
                content: '';
                display: block;
                top: 50%;
                right: 0.45rem;
                margin-top: -0.08rem;
                height: 0.15rem;
                width: 0.15rem;
                border-bottom: 0.04rem solid #fff;
                border-right: 0.04rem solid #fff;
                transform: rotateZ(-45deg);
                z-index: 2;
            }

            .photo {
                width: 0.79rem;
                height: 0.79rem;
                border-radius: 50%;
                background: url("../assets/images/icon_jiaru@3x.png") no-repeat center center;
                background-size: cover;
                margin-top: 0.28rem;
                margin-left: 0.34rem;
                float: left;
            }

            .center {
                margin: 0.34rem 0;
                padding-top: 0.26rem;
                overflow: hidden;
                div {
                    display: block;
                    width: 100%;
                    clear: both;
                    height: 0.4rem;
                    padding-right: 1.01rem;
                    padding-left: 0.27rem;
                }
                div:nth-child(1) {
                    span {
                        color: #FFFFFF;
                        font-size: 0.32rem;
                        text-align: left;
                        float: left;
                        font-weight: bold;
                        position: relative;

                    }
                    em {
                        float: right;
                        font-size: 0.24rem;
                        color: #FFFFFF;
                    }
                }
                div:nth-child(2) {
                    span, i {
                        color: rgba(255, 255 ,255, 0.5);
                        margin-right: 0.3rem;
                        font-size: 0.24rem;
                        text-align: left;
                        float: left;
                    }
                    em {
                        float: right;
                        font-size: 0.24rem;
                        color: rgba(255, 255 ,255, 0.5);
                    }
                    em.lastTime {
                        color: #DE4B43;
                    }
                }
            }
        }
    }

</style>