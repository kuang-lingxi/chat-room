<template>
    <div>
        <div id="sidebar" :style="right" @click="drawer = true">
            我的好友
        </div>

        <el-drawer
            title="好友列表"
            :visible.sync="drawer"
            :show-close="false"
        >
            <div class="title" @click="teacher=!teacher">
                <span class="el-icon-arrow-right"></span>
                <span class="font">老师</span>
            </div>
            <div v-if="teacher" class="teacher" >
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
            </div>
            <div class="title" @click="classmate=!classmate">
                <span class="el-icon-arrow-right"></span>
                <span class="font">同学</span>
            </div>
            <div v-if="classmate" class="classmate">
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
                <User
                    name="xxx"
                    introduce="我非常牛逼，非常非常非常牛逼，世界你好，你好世界，我不想在写代码了"
                />
            </div>
        </el-drawer>
    </div>
</template>

<script>
import User from './User'

export default {
    data() {
        return {
            right: {
                position: 'fixed',
                right: '0',
                top: this.top
            },
            drawer: false,
            teacher:false,
            classmate:false
        }
    },
    props:{
        left: {
            type: Boolean,
            default: false
        },
        top: {
            default: "20%"
        }
    },
    components: {
        User
    }
}
</script>

<style lang="scss" scoped>
    #sidebar {
        width: 20px;
        height: 100px;
        border-radius: 30px;
        border-top-right-radius: 0;
        border-bottom-right-radius: 0;
        background-color: #3d9afb;

        margin:0;
        padding:0;

        writing-mode: vertical-rl;
        text-align: center;
        line-height: 20px;

        &:hover {
           cursor: pointer; 
        }
    }
    .right {
        
    }
    .title {
        width:100%;
        padding: 20px 10px;
        background-color: #f8f8f8;
        margin-top:5px;

        .font {
            font-size: 15px;
            margin-left: 20px;
        }

        &:hover{
            cursor: pointer;
        }
    }
    .teacher,.classmate {
        height: 331px;
        overflow:scroll;
    }
</style>

