<template>
    <el-container direction="vertical">
        <nav-header></nav-header>
        <el-container  direction="horizontal">
            <el-aside style="background-color: rgb(84, 92, 100);width: 16.6666666667%">
                <left-menu></left-menu>
            </el-aside>
            <el-container direction="vertical">
                <el-main>
                    <h2 class="h2">自动回复</h2>
                    <nav-bread :nav-names="navBread">
                        <div slot="被添加自动回复">
                            <div class="purview-tips">
                                <p>*使用此功能需开启服务器配置。</p>
                                <p>&nbsp;通过编辑内容或关键词规则，快速进行自动回复设置。</p>
                            </div>
                            <el-tabs type="border-card" style="margin: 15px 0">
                                <el-tab-pane>
                                    <span slot="label"><i class="el-icon-date"></i>文字</span>
                                    <div class="emotion_editor">
                                        <div class="edit_area js_editorArea"
                                             contenteditable="true"
                                             id="text_area"
                                             style="overflow-y: auto;overflow-x: hidden;padding-bottom: 32px;">
                                        </div>
                                        <div class="editor_toolbar">
                                            <p class="editor_tip opr_tips"></p>
                                            <p class="editor_tip js_editorTip" id="text_length">还可以输入600字</p>
                                        </div>
                                    </div>
                                </el-tab-pane>
                                <el-tab-pane label="图片">图片</el-tab-pane>
                                <el-tab-pane label="音频">音频</el-tab-pane>
                                <el-tab-pane label="视频">视频</el-tab-pane>
                            </el-tabs>
                        </div>
                    </nav-bread>
                </el-main>
                <nav-footer></nav-footer>
            </el-container>
        </el-container>
    </el-container>
</template>
<style>
    h1,h2{
        font-weight: normal;
    }
    .h1{
        margin: 15px 0;
        font-size: 20px;
    }
    .h2{
        margin: 10px 0;
        font-size: 18px;
    }
    .purview-tips {
        background: #F0F0F0;
        padding: 9px 30px 6px;
        width: 100%;
        color: #FF7029;
    }
    .purview-tips p{
        font-size: 14px;
        line-height: 1.6;
    }
    .emotion_editor {
        position: relative;
        z-index: 1;
        border: 1px solid #e7e7eb;
        border-radius: 0;
        -moz-border-radius: 0;
        -webkit-border-radius: 0;
    }
    .emotion_editor .edit_area {
        padding: 14px 20px;
        outline: 0;
        word-wrap: break-word;
        word-break: break-all;
        border-top-left-radius: 0;
        -moz-border-radius-topleft: 0;
        -webkit-border-top-left-radius: 0;
        border-top-right-radius: 0;
        -moz-border-radius-topright: 0;
        -webkit-border-top-right-radius: 0;
        background-color: #fff;
        height: 280px;
    }
    .editor_toolbar {
        display: block;
        padding: 0 20px;
        line-height: 36px;
        background-color: #fff;
        position: absolute;
        right: 0;
        bottom: 0px;
    }
    .editor_tip {
        float: right;
        color: #8d8d8d;
        left: 0;
        right: 0;
        bottom: 0;
    }
</style>
<script>
    import NavHeader from '@/components/common/NavHeader'
    import NavFooter from '@/components/common/NavFooter'
    import LeftMenu from '@/components/common/LeftMenu'
    import NavBread from '@/components/common/NavBread'

    export default {
        data() {
            return {
                navBread: ['被添加自动回复','消息自动回复','关键词自动回复']
            }
        },
        components: {
            NavHeader,
            NavFooter,
            LeftMenu,
            NavBread
        }
    }
</script>
