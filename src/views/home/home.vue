<script setup>
import banner from './components/banner.vue'
import articleCard from './components/articleCard.vue'

const articleTest = {
    id: 1,
    title: 'HelloWorld',
    created: '2023/2/16 19:00:00',
    slug: 'HelloWorld',
    authorName: 'CairBin',
    browseCount: 1,
    typeName:'default'
}

</script>

<template>
    <div style="margin:0;padding:0;height:100%;width:100%;">
        <el-container style="height:100%;width:100%;">
            <el-header style="background-color:#f9f9f9;">

            </el-header>
            <el-main style="background-color:#f9f9f9;height:auto;padding:0;margin:0;">
                <el-row type="flex" justify="center" style="height:100%;width:100%;">
                    <el-col :span="4">

                    </el-col>
                    <el-col :span="16">
                        <banner></banner>
                        <div class="content-container">
                            <articleCard :obj="articleTest"></articleCard>
                        </div>
                    </el-col>
                    <el-col :span="4">

                    </el-col>
                </el-row>
            </el-main>
            <el-footer style="background-color:#edf1f2;">

            </el-footer>
        </el-container>
    </div>
</template>

<style scoped>
.content-container{
    margin-top:25px;
}
</style>