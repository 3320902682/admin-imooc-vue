<template>
  <div class="detail">
    <el-form>
      <sticky :z-index="10" :class-name="'sub-navbar'">
        <el-button v-if="!isEdit" @click.prevent.stop="showGuide">显示帮助</el-button>
        <el-button v-loading="loading" style="margin-left: 10px;" type="success" @click="submitForm">
          {{ isEdit ? '编辑电子书' : '新增电子书' }}
        </el-button>
      </sticky>
      <div class="detail-container">
        <el-row>
          <warning />
          <el-col :span="24">
            <!-- 编写具体表单控件 -->
          </el-col>
          <el-col :span="24">
            <!-- 编写具体表单控件 -->
          </el-col>
        </el-row>
      </div>
    </el-form>
  </div>
</template>

<script>
import Sticky from '../../../components/Sticky/index'
import Warning from './warning'
export default {
  name: 'Detail',
  components: { Warning, Sticky },
  props: {
    isEdit: { type: Boolean, detail: false }
  },
  methods: {
    /**
       * 显示帮组
       */
    showGuide() {

    },
    /**
       * 提交表单
       */
    submitForm() {

    }
  }
}
</script>

<style scoped lang="scss">

  .detail {
    position: relative;
    .detail-container {
      padding: 40px 45px 20px 50px;
      .preview-img {
        width: 200px;
        height: 270px;
      }
      .contents-wrapper {
        padding: 5px 0;
      }
    }
  }
</style>
