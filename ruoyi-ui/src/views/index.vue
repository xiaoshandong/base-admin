<template>
  <div class="app-container home">
    <el-row :gutter="20">
      <el-col :sm="24" :lg="24">
        <blockquote class="text-warning" style="font-size: 14px">
          <br />
          <!-- &nbsp;  -->
          <!-- <el-link href="http://txy.ruoyi.vip" type="primary" target="_blank"></el-link><br/> -->
          <!-- <h4 class="text-danger"></h4> -->
          <x-chart :id="id" :option="option"></x-chart>
          <br />
        </blockquote>
        <hr />
      </el-col>
    </el-row>
    <el-row :gutter="20">
      <el-col :sm="24" :lg="12" style="padding-left: 20px">
        <!-- <el-carousel :interval="4000" type="card" height="200px">
          <el-carousel-item v-for="item in 6" :key="item">
            <h3 class="medium">{{ item }}</h3>
          </el-carousel-item>
        </el-carousel> -->
        <h2></h2>
        <p></p>
        <p><b></b> <span>v{{ version }}</span></p>
        <!-- <p><el-tag type="danger">&yen;</el-tag></p> -->
        <!-- <p>
          <el-button
            type="primary"
            size="mini"
            icon="el-icon-cloudy"
            plain
            @click="goTarget('https://gitee.com/y_project/RuoYi-Vue')"></el-button>
          <el-button
            size="mini"
            icon="el-icon-s-home"
            plain
            @click="goTarget('http://ruoyi.vip')"></el-button>
        </p> -->
      </el-col>
      <el-col :sm="24" :lg="12" style="padding-left: 50px">
        <el-row>
          <el-col :span="12">
            <h2></h2>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="6">
            <h4></h4>
            <ul>
              <li></li>
              <li></li>
            </ul>
          </el-col>
          <el-col :span="6">
            <h4></h4>
            <ul>
              <li></li>
              <li></li>
            </ul>
          </el-col>
        </el-row>
      </el-col>
    </el-row>
    <el-divider />
    <el-row :gutter="20">
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span></span>
          </div>
          <div class="body">
            <p>
              <i class="el-icon-s-promotion"></i> <el-link href="http://www.ruoyi.vip"
                target="_blank"></el-link>
            </p>
            <p>
              <i class="el-icon-user-solid"></i> <s></s>
              <s></s> <s></s>
              <a href="https://jq.qq.com/?_wv=1027&k=4WWwqNxN" target="_blank"></a>
            </p>
            <p>
              <i class="el-icon-chat-dot-round"></i> <a href="javascript:;"></a>
            </p>
            <p>
              <i class="el-icon-money"></i><a href="javascript:;" class="支付宝信息"></a>
            </p>
          </div>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span></span>
          </div>
          <el-collapse accordion>
            <el-collapse-item title="">
              <ol>
                <li>1</li>
                <li>2</li>
              </ol>
            </el-collapse-item>
          </el-collapse>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span></span>
          </div>
          <div class="body">
            <!-- <img
              src="https://oscimg.oschina.net/oscnet/up-d6695f82666e5018f715c41cb7ee60d3b73.png"
              alt="donate"
              width="100%"
            /> -->
            <span style="display: inline-block; height: 30px; line-height: 30px"></span>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>

// 导入chart组件
import XChart from './components/chart.vue'
// 导入chart组件模拟数据
import options from '../chart-options/options'

export default {
  name: "index",
  data() {
    let option = options.bar
    return {
      // 版本号
      version: "1.0.0",
      id: 'test',
      option: option
    };
  },
  components: {
    XChart
 },
  methods: {
    goTarget(href) {
      window.open(href, "_blank");
    },
  },
};
</script>
<style scoped lang="scss">
#test {
 width: 50px;
 height: 100px;
 margin: 0px auto;
}
.home {
  blockquote {
    padding: 10px 20px;
    margin: 0 0 20px;
    font-size: 17.5px;
    border-left: 5px solid #eee;
  }
  hr {
    margin-top: 20px;
    margin-bottom: 20px;
    border: 0;
    border-top: 1px solid #eee;
  }
  .col-item {
    margin-bottom: 20px;
  }
  ul {
    padding: 0;
    margin: 0;
  }
  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;

    b {
      font-weight: 700;
    }
  }

  .update-log {
    ol {
      display: block;
      list-style-type: decimal;
      margin-block-start: 1em;
      margin-block-end: 1em;
      margin-inline-start: 0;
      margin-inline-end: 0;
      padding-inline-start: 40px;
    }
  }
}

  // .el-carousel__item h3 {
  //   color: #475669;
  //   font-size: 14px;
  //   opacity: 0.75;
  //   line-height: 200px;
  //   margin: 0;
  // }
  
  // .el-carousel__item:nth-child(2n) {
  //   background-color: #99a9bf;
  // }
  
  // .el-carousel__item:nth-child(2n+1) {
  //   background-color: #d3dce6;
  // }
</style>

