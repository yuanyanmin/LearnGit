<template>
    <div class="club">
        <div class="clubCenter">
            <h3>Club</h3>
            <div class="clubContent">
                <div class="create">
                    <button class="createClubBtn" @click="createClub">Create club
                    </button>
                    <button class="joinClubBtn" @click="joinClub">Join club</button>
                </div>
            </div>
        </div>

        <!--创建俱乐部-->
        <div class="createClub" v-if="isShowCreate" >
            <div class="createClubPrompt">
                <h3 class="title">Create club</h3>
                <a href="javascript:;"><span class="close-x" @click="closeCreate"></span></a>
                <div class="clubContent">
                    <p v-if="!info.protail_url">{{info.nickname.substr(0,1)}}</p>
                    <p v-else><img :src="info.portait_url" alt=""></p>
                    <a href="#" class="cUp" @click="changeImg">Click upload</a>
                    <div class="info">
                        <input type="text" :placeholder="plac1" @focus="focus1" @blur="blur1" v-model="text1">
                        <input type="text" :placeholder="plac2" @focus="focus2" @blur="blur2" v-model="text2">
                        <button>OK</button>
                    </div>
                </div>
            </div>
        </div>


        <!--加入俱乐部-->
        <div class="joinClub" v-show="isJoinClub">
            <div class="joinClubPrompt">
                <h3>Join Club</h3>
                <a href="javascript:;"><span class="close-x" @click="closeJoin"></span></a>
                <div class="joinContext">
                    <input type="text" :placeholder="plac3" @focus="focus3" @blur="blur3" v-model="text3">
                    <button>Join in</button>
                </div>
            </div>
        </div>
        
        <!--测试俱乐部-->
        
    </div>
</template>

<script>
    export default {
        name: "Club",
        data () {
            return {
                isShowCreate: false,
                isJoinClub: false,
                plac1: 'Club name',
                plac2: 'Club announcement',
                plac3: 'Club id',
                text1: '',
                text2: '',
                text3: '',
                info: {
                    nickname: 'User name',
                    eth_balance: 0,
                    eth_locked: 0,
                    eth_free: 0,
                    user_id: '',
                    role: 0,
                    protail_url: '',
                },
            }
        },
        methods: {
            createClub() {
                this.isShowCreate = true;

            },
            joinClub() {
                this.isJoinClub = true;
            },
            // 关闭按钮
            closeJoin() {
                this.isJoinClub = false;
            },
            closeCreate() {
                this.isShowCreate = false;
                console.log(this.isShowCreate);
            },

            // 创建弹窗
            // 上传头像
            changeImg() {

            },
            focus1() {
                this.plac1 = '';
            },
            focus2() {
                this.plac2 = '';
            },
            focus3() {
                this.plac3 = '';
            },
            blur1() {
                if(this.text1 === ''){
                    this.plac1 = 'Club name';
                }
            },
            blur2() {
                if(this.text2 === ''){
                    this.plac2 = 'Club announcement';
                }
            },
            blur3() {
                if(this.text3 === ''){
                    this.plac3 = 'Club id';
                }
            },
        },
    }
</script>

<style lang="less" scoped>
    .club {
        position: absolute;
        top: 0;
        left: 0;
        background-color: #1C1C4B;
        width: 100%;
        height: 100%;
        .clubCenter {
            width: 6.98rem;
            height: 6.02rem;
            border-radius: 0.12rem;
            text-align: center;
            background: linear-gradient(180deg,rgba(57,94,155,1),rgba(38,45,99,1));
            margin: 0.1rem auto 0 auto;
            h3 {
                height: 1.22rem;
                line-height: 1.22rem;
                font-size: 0.42rem;
                color: #CEE1FF;
            }
            .clubContent {
                background: #181840;
                width: 6.71rem;
                height: 4.66rem;
                margin: 0 auto;
                border-radius: 0.12rem;
                overflow: hidden;
                .create {
                    .createClubBtn, .joinClubBtn {
                        width: 5.87rem;
                        height: 1.32rem;
                        background: #43A64D;
                        border-radius: 0.09rem;
                        font-size: 0.4rem;
                        line-height: 1.32rem;
                        text-align: center;
                        margin: 0 auto;
                        color: #FFFFFF;
                        border: none;
                        outline: none;
                    }
                    .joinClubBtn {
                        margin-top: 0.31rem;
                    }
                    .createClubBtn {
                        margin-top: 0.94rem;
                    }
                }
            }
        }
        .joinClub {
            width: 100%;
            height: 100%;
            position: absolute;
            left: 0;
            top: 0;
            background: rgba(0, 0, 0, 0.75);
            .joinClubPrompt {
                width: 6.97rem;
                height: 5.10rem;
                background: linear-gradient(180deg,rgba(57,94,155,1),rgba(38,45,99,1));
                border-radius: 0.12rem;
                border: 0.01rem solid rgba(60,69,141,1);
                position: absolute;
                top: 50%;
                left: 50%;
                margin-left: -3.48rem;
                margin-top: -2.50rem;
                h3 {
                    height: 1.25rem;
                    line-height: 1.25rem;
                    font-size: 0.42rem;
                    color: #CEE1FF;
                    text-align: center;
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
                .joinContext {
                    width: 6.71rem;
                    height: 3.70rem;
                    background: rgba(24,24,64,1);
                    border-radius: 0.12rem;
                    margin: 0 auto;
                    text-align: center;
                    input {
                        width: 5.86rem;
                        height: 0.75rem;
                        border-bottom: 0.02rem solid #4A4A76;
                        margin-top: 1.04rem;
                        background: #181840;
                        outline: none;
                        padding-bottom: 0.3rem;
                        color: #E5E9E7;
                        font-size: 0.32rem;
                    }
                    button {
                        margin-top: 0.66rem;
                        width: 2.12rem;
                        height: 0.72rem;
                        border-radius: 0.09rem;
                        background: #CD3E4A;
                        color: #FFFFFF;
                        font-size: 0.36rem;
                        outline: none;
                        border: none;
                    }
                }
            }
        }
        .createClub {
            z-index: 999;
            position: absolute;
            top: 0;
            left: 0;
            background-color: rgba(0,0,0,0.75);
            height: 100%;
            width: 100%;
            .createClubPrompt {
                width: 6.97rem;
                height: 8.48rem;
                background: linear-gradient(180deg,rgba(57,94,155,1),rgba(38,45,99,1));;
                border-radius: 0.12rem;
                border: 0.01rem solid rgba(60,69,141,1);
                position: absolute;
                top: 50%;
                left: 50%;
                margin-left: -3.48rem;
                margin-top: -4.24rem;
                color: #000000;
                font-size: 0.4rem;
                text-align: center;
                .title {
                    height: 1.25rem;
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
                .clubContent {
                    width: 6.71rem;
                    height: 7.08rem;
                    background:rgba(24,24,64,1);
                    border-radius: 0.12rem;
                    margin: 0 auto;
                    overflow: hidden;
                    p {
                        width: 1.36rem;
                        height: 1.36rem;
                        border-radius: 1.36rem;
                        background: #B59B70;
                        border: 1px solid #979797;
                        margin: 0.52rem auto 0.30rem auto;
                        font-size: 0.68rem;
                        line-height: 1.36rem;
                        color: #FFFFFF;
                        img {
                            width: 100%;
                            border-radius: 100%;
                        }
                    }
                    .cUp {
                        font-size: 0.28rem;
                        color: #696994;
                    }
                    input {
                        width: 5.56rem;
                        color: #E5E9E7;
                        border-bottom: 0.03px solid #979797;
                        font-size: 0.32rem;
                        line-height: 0.56rem;
                        margin-top: 0.35rem;
                        padding-bottom: 0.23rem;
                        background-color: #181840;
                        text-align: left;
                    }
                    button {
                        width: 2.12rem;
                        height: 0.76rem;
                        background: #CD3E4A;
                        outline: none;
                        border: none;
                        font-size: 0.32rem;
                        margin-top: 0.72rem;
                        border-radius: 0.09rem;
                        color: #ffffff;
                        line-height: 0.76rem;
                    }
                }

            }
        }
    }
</style>
