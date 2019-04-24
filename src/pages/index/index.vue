<template>
  <div @click="clickHandle">
    <form id="indexSearchForm">
      <input type="text" id="indexSearch" class="indexSearch" placeholder="#儿童感冒快速应急#">
      <label for="indexSearch"></label>
      <img class="indexSearch-icon" style="height: 20px; width: 20px;" src="../../../static/images/search.png">
      <img class="indexMessage-icon" style="height: 35px; width: 35px;" src="../../../static/images/message.png">
    </form>
    <div id="searchIcon">
      <div class="searchIcon">
        <a href="/pages/counter/main">
          <img style="height: 50px; width: 50px;" src="../../../static/images/doctor.png" alt="医生">
        </a>
        <a href="/pages/counter/main">
          <p>医生</p>
        </a>

      </div>

      <div class="searchIcon">
        <a href="/pages/counter/main">
          <img style="height: 50px; width: 50px;" src="../../../static/images/hospital.png" alt="医院">
        </a>
        <a href="/pages/counter/main">
          <p>医院</p>
        </a>
      </div>
      <div class="searchIcon">
        <a href="/pages/counter/main">
          <img style="height: 50px; width: 50px;" src="../../../static/images/drug.png" alt="药品">
        </a>
        <a href="/pages/counter/main">
          <p>药品</p>
        </a>
      </div>
    </div>
    <div id="hotSearch">
      <span>热门搜索</span>
      <div id="hotSearch-link">
        <selfButton></selfButton>
        <selfButton></selfButton>
        <selfButton></selfButton>
        <selfButton></selfButton>
        <selfButton></selfButton>
        <selfButton></selfButton>
      </div>
    </div>


  </div>
</template>

<script>
import card from '@/components/card'
import selfButton from '@/components/selfButton'

export default {
  data () {
    return {
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card,
    selfButton
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
#indexSearchForm{
  position: relative;
  display: inline-block;
  left: 20px;
}
.indexSearch{
  left: 20px;
  width: 100%;
  line-height: 30px;
  font-size: 17px;
  padding: 10px 12px 10px 40px;
  border-radius: 5px;
  box-shadow: #999;
  background-color: #fafafa;
}
.indexSearch-icon{
  position: absolute;
  top: 30%;
  left: 10px;
}
.indexMessage-icon{
  position: absolute;
  top: 10%;
  left: 128%;
}
#searchIcon{
  position: relative;
  display: inline-block;
  text-align: center;
  overflow: hidden;
  zoom: 1;
  width: 100%;
  top: 20px;
}
.searchIcon{
  float: left;
  width: 33.3%;
  font-size: 14px;
}
#hotSearch{
  position: relative;
  top: 30px;
  left: 20px;
  font-size: 16px;
}
</style>
