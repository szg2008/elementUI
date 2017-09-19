<template>
  <div>
      <el-row>
          <el-col :span="24">
              <div class="grid-content bg-purple-dark danger">
                  Layout布局
              </div>
          </el-col>
      </el-row>
      <el-row>
          <el-col :span="24">
              <div class="grid-content bg-purple-dark">
              </div>
          </el-col>
      </el-row>
      <el-row>
          <el-col :span="12"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="12"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
      <el-row>
          <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="16"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
      <el-row :gutter="20">
          <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="16"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
      <el-row :gutter="24">
          <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="8" :offset="8"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
      <el-row type="flex" class="row-bg">
          <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
          <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row type="flex" class="row-bg" justify="space-between">
          <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
          <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>
      <el-row :gutter="10">
          <el-col :xs="8" :sm="6" :md="4" :lg="3"><div class="grid-content bg-purple"></div></el-col>
          <el-col :xs="4" :sm="6" :md="8" :lg="9"><div class="grid-content bg-purple-light"></div></el-col>
          <el-col :xs="4" :sm="6" :md="8" :lg="9"><div class="grid-content bg-purple"></div></el-col>
          <el-col :xs="8" :sm="6" :md="4" :lg="3"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
      <el-row>
          <el-col :span="24">
              <div class="grid-content bg-purple-dark danger">
                  Icon图标
              </div>
          </el-col>
      </el-row>
      <i class="el-icon-edit"></i>
      <i class="el-icon-check"></i>
      <i class="el-icon-more"></i>
      <i class="el-icon-setting"></i>
      <i class="el-icon-time"></i>
      <i class="el-icon-loading"></i>
      <br>
      <br>
      <el-row>
          <el-col :span="24">
              <div class="danger grid-content bg-purple-light">
                  Button按钮
              </div>
          </el-col>
      </el-row>
      <el-button :disabled="true">默认按钮</el-button>
      <el-button type="text">文字按钮</el-button>
      <el-button type="danger" >危险按钮</el-button>
      <br>
      <br>
      <el-button type="warning" icon="edit"></el-button>
      <el-button type="primary" icon="setting">设置按钮</el-button>
      <el-button type="danger" :loading="true">加载中</el-button>
      <br>
      <br>
      <el-button type="primary" icon="setting" size="small">设置按钮</el-button>
      <el-button-group>
          <el-button type="primary" icon="arrow-left">上一页</el-button>
          <el-button type="primary">下一页<i class="el-icon-arrow-right el-icon--right"></i></el-button>
      </el-button-group>
      <br>
      <br>
      <el-row>
          <el-col>
              <div class="danger grid-content bg-purple">
                  单选按钮
              </div>
          </el-col>
      </el-row>
  </div>
</template>

<script>
export default {

}
</script>
<style>
.danger{background-color: #13CE66 !important;}
.el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
}
.el-col {
    border-radius: 4px;
}
.bg-purple-dark {
    background: #99a9bf;
}
.bg-purple {
    background: #d3dce6;
}
.bg-purple-light {
    background: #e5e9f2;
}
.grid-content {
    border-radius: 4px;
    min-height: 36px;
    line-height: 36px;
    padding:0 10px;
    color:#fff;
}
</style>
