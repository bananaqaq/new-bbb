<template>
  <div class="head-container">
    <section class="head-title">
      <div class="head-title-logo">NEW BBB</div>
      <div>币币交易</div>
      <div>杠杆交易</div>
      <div>合约交易</div>
    </section>
    <section class="head-opt">
      <div>
        <Button>登录</Button>
        <Button type="primary">注册</Button>
      </div>
      <div>
        <Icon type="md-volume-down" size="22"/>
      </div>
      <div>
        <Icon type="md-settings" size="22"/>
      </div>
      <div>
        <Select v-model="sysLanguage" style="width:80px;">
          <Option value="ch" key="ch">中文</Option>
          <Option value="en" key="en">English</Option>
        </Select>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data(){
    return {
      sysLanguage: "ch",
    }
  }
};
</script>

<style>
.head-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.head-container .head-title{
  display: flex;
  align-items: center;
  justify-content: space-between;
  color:#ffffff;
  font-size: 14px;
}
.head-container .head-title >div{
  margin-right: 35px;
}
.head-container .head-title .head-title-logo{
  color:#ffffff;
  font-size:26px;
  font-weight: 600;
  margin-right: 55px;
}
.head-container .head-opt{
  display: flex;
  align-items: center;
  justify-content: space-between;
  color:#ffffff;
  font-size: 14px;
}
.head-container .head-opt >div{
  border-right: 1px solid #ffffff;
  height: 40px;
  padding-left: 18px;
  padding-right:18px;
  display: flex;
  align-items: center;
}
.head-container .head-opt >div:nth-of-type(4){
  border-right: 0px none #ffffff;
}
.head-container .head-opt >div button:nth-of-type(1){
  margin-right: 10px;
}

</style>
