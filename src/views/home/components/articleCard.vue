<script setup>
import { defineProps } from 'vue'

const props = defineProps({
    obj: {
        id: {
            type: Number,
            require: true
        },
        title: {
            type: String,
            require: true,
            default: 'HelloWorld'
        },
        slug: {
            type: String,
            require: true,
            default: ''
        },
        authorName: {
            type: String,
            require: true,
            default: 'CairBin'
        },
        browseCount: {
            type: Number,
            require: true,
            default: 0
        },
        created: {
            type: Date,
            require: true
        },
        typeName: {
            type: String,
            require: true,
            default: 'default'
        }
    }
})

</script>

<template>
    <el-card class="card" shadow="hover">
        <div class="post-title">
            <router-link v-bind:to="'/post/'+ props.obj.id">
                {{props.obj.title}}
            </router-link>
        </div>
        <div class="post-slug">
            {{ props.obj.slug }}
        </div>
        <div class="post-meta">
            <i class="el-icon-user"><a href="http://www.baidu.com">{{ props.obj.authorName }}</a></i><el-divider direction="vertical"></el-divider>
            <i class="el-icon-view">{{ props.obj.browseCount }}</i><el-divider direction="vertical"></el-divider>
            <i class="el-icon-chat-line-round">评论</i><el-divider direction="vertical"></el-divider>
            <i class="el-icon-alarm-clock"><a href="http://www.baidu.com">{{ props.obj.created }}</a></i>
        </div>
        <div class="post-tag">
            <i class="el-icon-collection-tag"></i>&nbsp;
            <el-tag v-if="props.obj.typeName != null">{{ props.obj.typeName }}</el-tag>
            <el-tag v-else>默认分类</el-tag>
        </div>
    </el-card>
</template>

<style scope>
.card{
    background: rgba(255, 255, 255, 0.9);
    height: auto;
    border-radius: 10px;
}

.post-title a{
    font-size: 32px;
    letter-spacing: 0.5px;
    color: #F56C6C;
    transition: all 0.35s ease;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-decoration: none;
}

.post-title a:hover{
    letter-spacing: 1px;
}

.post-meta {
    margin-top: 10px;
    font-size: 1.2rem;
}

.post-meta a{
    color: black;
    text-decoration: none;
}

.post-slug {
    margin-top: 10px;
    font-size: 1.2rem;
    line-height: 1.8;
    margin-bottom: 10px;
    height:90px;
    overflow: hidden;
    text-overflow:ellipsis;
}

.post-slug p {
    font-weight: normal;
}

.post-tag{
    margin-top:10px;
    font-size: 1.2rem;
}
</style>