<template>
  <div class="doc">
    <div class="doc-nav">
      <ul class="main-menu">
        <li>
          <router-link :to="{path:'#base'}">基础</router-link>
          <ul class="nav-dropdown">
            <li>
              <router-link :to="{path:'#start'}">开始</router-link>
            </li>
            <li>
              <router-link :to="{path:'#dongtai'}">动态路由</router-link>
            </li>
            <li>
              <router-link :to="{path:'#qiantaoluyou'}">嵌套路由</router-link>
            </li>
          </ul>
        </li>
        <li>
          <router-link :to="{path:'#jinjie'}">进阶</router-link>
          <ul class="nav-dropdown">
            <li>
              <router-link :to="{path:'#jinjie1'}">导航钩子</router-link>
            </li>
            <li>
              <router-link :to="{path:'#jinjie2'}">路由元信息</router-link>
            </li>
            <li>
              <router-link :to="{path:'#jinjie3'}">过渡动效</router-link>
            </li>
          </ul>
        </li>
      </ul>
    </div>
    <div class="doc-view">
      <doc-view></doc-view>
    </div>
  </div>
</template>

<script>
    import docView from '@/views/doc-view'
    import TWEEN from 'tween.js'
    export default {
        name: "doc",
        data(){
          return{

          }
        },
        methods:{

        },
        mounted(){
            console.log('d',this.$fff)
        },
        components:{
          docView,
          TWEEN
        }
    }
</script>
tween
<style scoped>
  li{
    list-style: none;
  }
  .doc {
    position: fixed;
    top: 100px;
    left: 280px;
    right: 0;
    bottom: 0;
    z-index: 1;
    overflow-y: scroll;
  }
  .doc-nav {
    position: fixed;
    z-index: 10;
    top: 100px;
    left: 0;
    bottom: 0;
    padding: 0px 0 30px 60px;
    width: 200px;
    margin-right: 20px;
    overflow-x: hidden;
    overflow-y: auto;
    background: #fff;
  }

  .doc-nav .main-menu {
    margin-bottom: 20px;
    padding-left: 0;
    line-height: 1.8em;
  }

  .main-menu ul {
    list-style-type: none;
    margin: 0;
    padding-left: 1em;
  }

  .main-menu ul span {
    color: #7f8c8d;
  }


  .main-menu ul a {
    font-weight: bold;
  }

  .doc-view {
    position: relative;
    padding: 2.2em 0;
  }

</style>
