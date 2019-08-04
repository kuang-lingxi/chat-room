<template>
    <el-row class="main">
        <el-col :span="3" style="overflow:hidden">
            <el-avatar
                :src="imgUrl"
            ></el-avatar>
        </el-col>
        <el-col :span="19" style="overflow:hidden">
            <div class="name">{{name}}</div>
            <div class="introduce">{{introduce}}</div>
        </el-col>
    </el-row>    
</template>

<script>
export default {
    props: ['imgUrl', 'name', 'introduce']
}
</script>

<style lang="scss" scoped>
    .main {
        width: 100%;
        padding: 5% 5%;
        /* background-color: #9ad7fd; */

        &:hover {
            cursor: pointer;
        }
    }
    .name {
        font-weight: bold;
    }
    .introduce {
        text-indent: 10px;
        font-size: 10px;
        color: #cccccc;

        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
</style>
