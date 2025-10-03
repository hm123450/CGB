<script lang="ts" setup>
import { ElIcon } from 'element-plus'
import { Document, Files, MagicStick, Picture, DataAnalysis, Film } from '@element-plus/icons-vue'

// logo地址，没有则置为""即可
const logo = ''

// 标题
const title = 'ChangingGrounding: 3D Visual Grounding in Changing Scenes'

// 标题颜色
const title_color = '#000000'

// 标题补充，没有则置为''即可
const title_supp = ''

// 标题补充颜色
const title_supp_color = '#42B883'

// 按钮颜色
const btn_color = '#444444'

// 作者清单（只保留名字和上标，不用头像）
const authors = [
  {
    name: "Miao Hu",
    homepage: "https://github.com/hm123450",
    address_flag: "1"
  },
  {
    name: "Zhiwei Huang",
    homepage: "https://github.com/huang583824382",
    address_flag: "2"
  },
  {
    name: "Tai Wang",
    homepage: "https://tai-wang.github.io",
    address_flag: "4"
  },
  {
    name: "Jiangmiao Pang",
    homepage: "https://oceanpang.github.io",
    address_flag: "4"
  },
  {
    name: "Dahua Lin",
    homepage: "http://dahua.site",
    address_flag: "3,4"
  },
  {
    name: "Nanning Zheng",
    homepage: "http://www.aiar.xjtu.edu.cn/info/1046/1229.htm",
    address_flag: "1,*"
  },
  {
    name: "Runsen Xu",
    homepage: "https://runsenxu.com",
    address_flag: "3,4,*"
  }
]

// 地址清单（只保留文字，不用图标）
const addresses = [
  {
    address_flag: "1",
    name: "Xi’an Jiaotong University",
    homepage: "https://www.xjtu.edu.cn/"
  },
  {
    address_flag: "2",
    name: "Zhejiang University",
    homepage: "https://www.zju.edu.cn/"
  },
  {
    address_flag: "3",
    name: "The Chinese University of Hong Kong",
    homepage: "https://www.cuhk.edu.hk/"
  },
  {
    address_flag: "4",
    name: "Shanghai AI Laboratory",
    homepage: "https://www.shlab.org.cn/"
  },
]

// 共一和通讯提示
const con_and_corresponding_author = 
  "*: Corresponding Author."

// 提供引导资料链接
const buttons = [
  {
    disabled: true,
    name: "Paper",
    component: Document,
  },
  {
    disabled: false,
    name: "Code",
    link: "https://github.com/xxx/xxx",
    component: Files,
  },
  {
    disabled: false,
    name: "Demo",
    link: "https://xxx/demo",
    component: MagicStick,
  }
]
</script>

<template>
  <div>
    <!-- 文章标题 -->
    <el-row justify="center">
      <el-col :span="20">
        <h1 class="paper-title">
          <span v-if="title" :style="{color:title_color}">{{ title }}</span>
          <span v-if="title_supp" :style="{color:title_supp_color}">{{ title_supp }}</span>
        </h1>
      </el-col>
    </el-row>

    <!-- 作者名单（去掉头像） -->
    <el-row justify="center">
      <a :href="author.homepage" v-for="author in authors" :key="author.name">
        <el-button class="title-button" type="primary" text>
          <span class="author">
            {{ author.name }}<sup v-if="author.address_flag" class="name_sup">{{ author.address_flag }}</sup>
          </span>
        </el-button>
      </a>
    </el-row>

    <!-- 地址名单（去掉头像） -->
    <el-row justify="center">
      <a :href="address.homepage" v-for="address in addresses" :key="address.name">
        <el-button class="title-button" type="primary" text>
          <span class="address">
            <sup v-if="address.address_flag" class="address_sup">{{ address.address_flag }}</sup>{{ address.name }}
          </span>
        </el-button>
      </a>
    </el-row>

    <!-- 共一和通讯提示 -->
    <el-row justify="center" class="con-cor">
        {{ con_and_corresponding_author }}
    </el-row>

    <!-- 提供引导按钮 -->
    <el-row justify="center" style="margin-bottom: 20px;">
      <el-col :span="20">
        <el-row justify="center">
          <a :href="button.link" v-for="button in buttons" :key="button.name">
            <el-button class="guidance-button" size="default" :color="btn_color" :disabled="button.disabled" round>
              <el-icon :size="18">
                <component :is="button.component" />
              </el-icon>
              <span class="btn-text">{{ button.name }}</span>
            </el-button>
          </a>
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.paper-title {
  font-family: "MyFont", Verdana, sans-serif;
  letter-spacing: 2px;
  font-size: 42px;
  margin: 32px;
  text-align: center;
}
.title-button {
  margin: 10px 3px;
}
.title-button:hover {
  margin: 10px 8px;
}
.guidance-button {
  margin: 8px 5px;
  box-shadow: #d8d8d8 1px 1px 1px 1px;
}
.author {
  font-size: 18px;
  margin-left: 3px;
}
.name_sup {
  color: #606266; 
  margin-left: 3px;
}
.address {
  font-size: 18px;
}
.address_sup {
  color: #606266; 
  margin-right: 1px;
}
.con-cor {
  font-family: Arial;
  font-size: 14px;
  margin: 18px 0px;
  text-align: center;
}
.btn-text {
  font-size: 18px;
  color: #ffffff;
}
</style>
