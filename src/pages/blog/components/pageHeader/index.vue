<template>
    <el-form
            :inline="true"
            ref="form"
            size="mini"
            style="margin-bottom: -18px;">
        <el-form-item>
            <el-button type="primary"
                       @click="handleFormArticle">
                <d2-icon name="pencil"/>
                写文章
            </el-button>
        </el-form-item>
    </el-form>
</template>

<script>
    export default {
        props: {
            isMulti: {
                type: Boolean,
                default: true
            }
        },
        methods: {
            handleFormArticle() {
                this.$emit('onArticle')
            },
            handleFormArticleDel() {
                this.$emit('onPatchDelete')
            }
        }
    }
</script>
