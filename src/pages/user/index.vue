<template>
  <div @click="clickHandle">
    <div>
      <div id="user">
        <div id="userMessage">
          <img style="height: 100px; width: 100px;" src="../../../static/images/person.png">
          <span>余生</span>
          <a href="#"><img class="userMessage-icon" style="height: 40px; width: 40px;" src="../../../static/images/message.png"></a>
        </div>
      </div>
      <div id="dianZiBinLi">
        <userMessage></userMessage>
        <userMessage></userMessage>
        <userMessage></userMessage>
        <userMessage></userMessage>
      </div>
      <div class="description">
        <article>
          <p>小程序版本：1.0.0</p>
          <p>家庭医生小程序暂时属于个人娱乐，没有任何授权</p>
        </article>
      </div>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'
import selfButton from '@/components/selfButton'
import userMessage from '@/components/userMessage'

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
    selfButton,
    userMessage
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
page{
  background-color: #fafafa;
}
#user{
  background-color: #ccc;
}
#userMessage{
  display: inline-block;
  position: relative;
  height: 100px;
}
#userMessage img{
  float: left;
  border-radius: 50px;
  margin: 20px 0 0 20px;
}
#userMessage span{
  float: left;
  padding-top: 40%;
  padding-left: 20px;
  font-size: 20px;
}
.userMessage-icon{
  position: absolute;
  left: 165%;
}
.description{
  position: relative;
  color: #999;
  top: 30px;
  font-size: 14px;
}
.description article p{
  padding: 10px 0 0 0;
}
</style>
