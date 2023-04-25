<script setup>

</script>

<template>
    <div class="banner">
        <el-row  type="flex" justify="center">
            <el-col :span="24">
                <div class="banner-logo">
                    <el-avatar class="banner-logo-img" :size="100" src="https://cairbin.gitee.io/cair_img/img/bloglogo.png">
                    </el-avatar>
                </div>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center">
            <el-col :span="24">
                    <div>
                        <div class="banner-text">CairBin</div>
                        <div class="banner-text banner-description">
                            To be or not to be ...
                        </div>
                    </div>
                </el-col>
        </el-row>
        <el-row type="flex" justify="center">
            <el-space spacer="|">
                <el-link type="primary">主页</el-link>
                <el-link type="success">友链</el-link>
                <el-link type="warning">分类</el-link>
                <el-link type="danger">归档</el-link>
                <el-link type="info">关于</el-link>
            </el-space>
        </el-row>
    </div>
</template>

<style scoped>
.banner{
    width:100%;
    height:180px;
    background:rgb(0,0,0,0);
    color:#777777;
}

.banner .banner-logo{
    display: flex;
    justify-content: center;
    align-content: center;
    width:100%;
}

.banner .banner-text{
    text-align:center;
    font-size:1.8em;
    margin-bottom:10px;
}

.banner .banner-description{
    font-size:1.1em;
    overflow: hidden;
    white-space: nowrap;
}

.el-row{
    width:100%;
    margin-bottom: 10px;
}

</style>