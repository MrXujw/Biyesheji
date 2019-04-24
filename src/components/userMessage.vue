<template>
  <div class="button">
    <a href="#">
      <div class="button-link">
        <span>{{ name }}</span>
        <img class="message-link" style="height: 20px; width: 20px;" src="../../static/images/jiantou1.png">
      </div>
    </a>
  </div>
</template>
<script>
module.exports = {
  data: function () {
    return {
      name: '电子病历'
    }
  }
}
</script>
<style scoped>
.button{
  position: relative;
  top: 30px;
  padding-bottom: 10px;
}
.button-link{
  position: relative;
  border: none;
  padding: 0 10px 0 10px;
  font-size: 16px;
  background-color: white;
  line-height: 50px;
}
.message-link{
  position: absolute;
  top: 33.3%;
}
</style>
