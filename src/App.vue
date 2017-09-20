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
                  单选按钮、多选按钮
              </div>
          </el-col>
      </el-row>
      <el-radio label="1" v-model="radio" disabled>选项一</el-radio>
      <el-radio label="2" v-model="radio">选项二</el-radio>
      <el-radio-group v-model="radio2">
          <el-radio :label="4">选项一</el-radio>
          <el-radio :label="5">选项二</el-radio>
          <el-radio :label="6">选项三</el-radio>
      </el-radio-group>
      <br>
      <br>
      <el-radio-group v-model="radio3" size="large">
          <el-radio-button label="北京"></el-radio-button>
          <el-radio-button label="上海"></el-radio-button>
          <el-radio-button label="广州" disabled></el-radio-button>
          <el-radio-button label="深圳"></el-radio-button>
      </el-radio-group>
      <br>
      <br>
      <el-checkbox v-model="checkbox" disabled>多选一</el-checkbox>
      <el-checkbox-group v-model="checkList">
          <el-checkbox label="北京">北京</el-checkbox>
          <el-checkbox label="上海">上海</el-checkbox>
          <el-checkbox label="杭州">杭州</el-checkbox>
          <el-checkbox label="成都" disabled>成都</el-checkbox>
      </el-checkbox-group>
      <br>
      <el-checkbox-group v-model="checkList" :min="2" :max="3">
          <el-checkbox v-for="city in checkList1" :label="city" :key="city">{{city}}</el-checkbox>
      </el-checkbox-group>
      <br>
      <el-checkbox-group v-model="checkList" size="large" fill="#324057" text-color="#a4aebd" :min="1" :max="3">
          <el-checkbox-button v-for="city in checkList1" :label="city" :key="city">{{city}}</el-checkbox-button>
      </el-checkbox-group>
      <br>
      <el-row>
          <el-col>
              <div class="danger grid-content bg-purple">
                  输入框
              </div>
          </el-col>
      </el-row>
      <el-input placeholder="输入内容" :disabled="true"></el-input>
      <br>
      <br>
      <el-input placeholder="输入内容" icon="search"></el-input>
      <br>
      <br>
      <el-input placeholder="输入内容" type="textarea" :row="3"></el-input>
      <br>
      <br>
      <el-input placeholder="请输入内容" v-model="input3">
          <template slot="prepend">Http://</template>
      </el-input>
      <br><br>
      <el-input placeholder="请输入内容" v-model="input4">
          <template slot="append">.com</template>
      </el-input>
      <br><br>
      <el-input placeholder="请输入内容" v-model="input5">
          <el-select slot="prepend" placeholder="请选择" v-model="select">
              <el-option label="餐厅名" value="1"></el-option>
              <el-option label="订单号" value="2"></el-option>
              <el-option label="用户电话" value="3"></el-option>
          </el-select>
          <el-button slot="append" icon="search"></el-button>
      </el-input>
      <br><br>
      <el-input-number :min="1" :max="15" @change="handleInputNumberChange" v-model="inputnumber"></el-input-number>
      <br><br>
      <el-row>
          <el-col>
              <div class="danger grid-content bg-purple">
                  选择框、开关、滑块
              </div>
          </el-col>
      </el-row>
      <el-select v-model="selectvalue" placeholder="请选择" >
          <el-option
              v-for="item in selectoptions"
              :key="item.value"
              :label="item.label"
              :value="item.value"
              :disabled="item.disabled"
          >
            </el-option>
      </el-select>
      <el-switch
        v-model="value2"
        on-color="#13ce66"
        off-color="#ff4949">
      </el-switch>
      <el-slider v-model="value1"></el-slider>
      <br><br>
      <el-row>
          <el-col>
              <div class="danger grid-content bg-purple">
                  时间日期选择器
              </div>
          </el-col>
      </el-row>
      <el-date-picker
        v-model="value21"
        type="datetime"
        placeholder="选择日期时间"
        align="right"
        :picker-options="pickerOptions1">
     </el-date-picker>
     <br><br>
     <el-row>
         <el-col>
             <div class="danger grid-content bg-purple">
                 上传、颜色选择
             </div>
         </el-col>
     </el-row>
     <el-upload
          action=""
          list-type="picture-card"
          :on-preview="handlePictureCardPreview"
          :on-remove="handleRemove">
          <i class="el-icon-plus"></i>
     </el-upload>
     <el-dialog v-model="dialogVisible" size="tiny">
          <img width="100%" :src="dialogImageUrl" alt="">
     </el-dialog>
     <br><br>
     <el-color-picker show-alpha></el-color-picker>
     <br>
     <el-row>
         <el-col>
             <div class="danger grid-content bg-purple">
                 表格、标签
             </div>
         </el-col>
     </el-row>
     <el-table
        :data="tableData"
        border
        style="width: 100%">
        <el-table-column
          prop="date"
          label="日期"
          width="180">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          width="180">
        </el-table-column>
        <el-table-column
          prop="address"
          label="地址">
        </el-table-column>
    </el-table>
    <br>
    <el-tag type="success">标签四</el-tag>
    <el-tag type="warning">标签三</el-tag>
  </div>
</template>
<script>
export default {
    data(){
        return {
            radio:"2",
            radio2:5,
            radio3:"上海",
            checkbox:true,
            checkList:['杭州','上海'],
            checkList1:['杭州','上海','北京','太原'],
            input3:'',
            input4:'',
            input5:'',
            select:'',
            inputnumber:'1',
            selectoptions: [{
              value: '选项1',
              label: '黄金糕'
            }, {
              value: '选项2',
              label: '双皮奶',
              disabled:true
            }, {
              value: '选项3',
              label: '蚵仔煎'
            }, {
              value: '选项4',
              label: '龙须面'
            }, {
              value: '选项5',
              label: '北京烤鸭'
            }],
            selectvalue: '',
            value2:'true',
            value1:20,
            pickerOptions1: {
                shortcuts: [{
                    text: '今天',
                    onClick(picker) {
                      picker.$emit('pick', new Date());
                    }
                  }, {
                    text: '昨天',
                    onClick(picker) {
                      const date = new Date();
                      date.setTime(date.getTime() - 3600 * 1000 * 24);
                      picker.$emit('pick', date);
                    }
                  }, {
                    text: '一周前',
                    onClick(picker) {
                      const date = new Date();
                      date.setTime(date.getTime() - 3600 * 1000 * 24 * 7);
                      picker.$emit('pick', date);
                    }
                  }]
            },
            value21:'',
            dialogImageUrl: '',
            dialogVisible: false,
            tableData: [{
              date: '2016-05-02',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1518 弄'
            }, {
              date: '2016-05-04',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1517 弄'
            }, {
              date: '2016-05-01',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1519 弄'
            }, {
              date: '2016-05-03',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1516 弄'
            }]
        }
    },
    method:{
        handleInputNumberChange(value){
            console.log(value)
        },
        handleRemove(file, fileList) {
            console.log(file, fileList);
        },
        handlePictureCardPreview(file) {
            this.dialogImageUrl = file.url;
            this.dialogVisible = true;
        }
    }
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
