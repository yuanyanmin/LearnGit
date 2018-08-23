<template>
    <div class="ClubManagement">
        <v-back><span :style="{textIndent:'-0.3rem',paddingRight:0}" class="title">Club Management</span></v-back>
        <p v-if="!info.protail_url">{{info.nickname.substr(0,1)}}</p>
        <p v-else><img :src="info.portait_url" alt=""></p>
        <div class="info">
            <div>
                <span>Club Name</span>
                <input type="text" placeholder="xhshsghhsh12534">
            </div>
            <div>
                <span>Club ID</span>
                <input type="text" placeholder="xhshsghhsh12534">
            </div>
            <div>
                <span>Club Notice</span>
                <input type="text" placeholder="xhshsghhsh12534">
            </div>
            <button>{{btnInfo}}</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ClubManagement",
        data() {
            return {
                info: {
                    nickname: 'User name',
                    eth_balance: 0,
                    eth_locked: 0,
                    eth_free: 0,
                    user_id: '',
                    role: 0,
                    protail_url: '',
                },
                btnInfo: '解散俱乐部',
            }
        }
    }
</script>

<style lang="less" scoped>
    .ClubManagement {
        .title {
            font-size: 0.38rem;
            font-weight: bold;
            color: #232F3C;
        }
        p {
            width: 1.8rem;
            height: 1.8rem;
            border-radius: 0.9rem;
            background: #B59B70;
            text-align: center;
            line-height: 1.8rem;
            color: #FFFFFF;
            font-size: 0.87rem;
            margin: 0.98rem auto 1.12rem auto;
            img {
                border-radius: 100%;
                margin: 0;
                width: 100%;
                display: block;
            }
        }
        .info {
            div {
                font-size: 0.34rem;
                color: #4A4A4A;
                height: 1.2rem;
                border-bottom: 0.01rem solid #E8E8E8;
                padding-top: 0.44rem;
                position: relative;
                span {
                    margin-left: 0.62rem;
                }
                input {
                    float: right;
                    margin-right: 0.96rem;
                    text-align: right;
                    font-size: 0.28rem;
                    color: #9B9B9B;
                }
                &:after {
                    position: absolute;
                    content: '';
                    display: block;
                    top: 50%;
                    right: 0.58rem;
                    margin-top: -0.1rem;
                    height: 0.26rem;
                    width: 0.26rem;
                    border-bottom: 0.04rem solid #9B9B9B;
                    border-right: 0.04rem solid #9B9B9B;
                    transform: rotateZ(-45deg);
                    z-index: 2;
                }
            }
            button {
                width: 6.31rem;
                height: 0.99rem;
                border-radius: 0.04rem;
                border: 0.02rem solid rgba(219,219,219,1);
                background: #FFFFFF;
                font-size: 0.42rem;
                margin: 0.8rem 0.61rem 0 0.58rem;
            }

        }
    }

</style>