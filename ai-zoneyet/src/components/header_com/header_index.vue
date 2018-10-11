<template>
  <section class="header_index">
    <div class="header_nav">
      <ul>
        <li class="header_img">

          <a href="#/"> <img src="../../assets/uishouye/Group 72.png" alt=""></a>
        </li>
       <div>
         <li v-for="(nav,index) in nav_data" :key="index">
           <p><a :href="'#'+nav.routerUp">{{nav.rootTitle}}</a></p>
           <div class="pull_down" v-show="nav.title.length>0">
             <p v-for="(pull_data,index) in nav.title" :key="index"><router-link :to="pull_data.nameUrl">{{pull_data.titleName}}</router-link></p>
           </div>
         </li>
       </div>

      </ul>
    </div>
  </section>
</template>

<script>
  export default {
    name: "header_index",
    data() {
      return {
        nav_data: [
          {
            rootTitle: '首页',
            routerUp:'/',
            title: []
          },
          {
            rootTitle: '关于我们',
            routerUp:'/aboutUs',
            title: [
              {titleName:'关于中业',nameUrl:'/aboutUs/zoneyet'},
              {titleName:'企业资质',nameUrl:'/aboutUs/Qualifications'}
            ]
          },
          {
            rootTitle: '翻译类别',
            routerUp:'/translateKind',
            title: [
              {titleName:'笔译',nameUrl:'/translateKind/W_translate'},
              {titleName:'口译',nameUrl:'/translateKind/O_translate'},
              {titleName:'本地化',nameUrl:'/translateKind/O_translate'},
              {titleName:'影视剧翻译',nameUrl:'/translateKind/M_translate'}
            ]
          },
          {
            rootTitle: '服务项目',
            routerUp:'/severProject',
            title: [
              {titleName:'翻译语种',nameUrl:'/severProject/languages'},
              {titleName: '翻译领域',nameUrl:'/severProject/field'},
              {titleName:'翻译流程',nameUrl:'/severProject/process'}
            ]
          },
          {
            rootTitle: '合作客户',
            routerUp:'/withCustomers',
            title: []
          },
          {
            rootTitle: '联系我们',
            routerUp:'/callUs',
            title: []
          },
        ]

      }
    },
  }
</script>

<style scoped>
  @import "./header_index.css";
</style>
