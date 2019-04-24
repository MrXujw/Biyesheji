<template>
  <div class="button">
    <div class="button-link">
      <a><img style="height: 15px; width: 15px; vertical-align: baseline;" src="../../static/images/hot.png">{{ name }}</a>
    </div>
  </div>
</template>
<script>
module.exports = {
  data: function () {
    return {
      name: '小儿感冒'
    }
  }
}
</script>
<style scoped>
.button{
  position: relative;
  display: inline-block;
  line-height: 30px;
  top: 10px;
  padding: 0 10px 10px 0;
}
.button-link{
  border: none;
  padding: 0 10px 0 10px;
  border-radius: 20px;
  font-size: 14px;
  color: gray;
  background-color: #fafafa;
}
</style>
