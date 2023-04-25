<script setup>
import banner from './components/banner.vue'

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

</style>