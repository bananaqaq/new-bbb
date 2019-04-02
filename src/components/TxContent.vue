<template>
    <div class="tx_container">
      <Card class="trading_market_card">
        <div slot="title" class="trading_market_card_head">
          <Row type="flex" justify="start" align="middle">
            <div class="symbol_name">
              BTC/USDT
            </div>
            <div class="price_container">
              <span>4648.29</span>
              <span>≈3126.10CNY</span>
            </div>
            <div class="change">
              <span>涨幅</span>
              <span>+12.14%</span>
            </div>
            <div class="high">
              <span>最高价</span>
              <span>5000.00</span>
            </div>
            <div class="low">
              <span>最低价</span>
              <span>4118.65</span>
            </div>
            <div class="amount">
              <span>24H量</span>
              <span>45,603 BTC</span>
            </div>
          </Row>
        </div>
        xxxx
      </Card>
      <Tabs value="name1" class="tx_opt_tab">
          <TabPane label="限价交易" name="name1">
            <Row class="tx_opt_tab_row">
              <Col span="12">
                <Form :label-width="50">
                  <FormItem label="买入价">
                    <Input>
                      <span slot="append">USDT</span>
                    </Input>
                  </FormItem>
                  <FormItem label="买入量">
                    <Input>
                      <span slot="append">&nbsp;IOTA&nbsp;</span>
                    </Input>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Slider v-model="buyaAmtPercent" :tip-format="formatAmtPercent"></Slider>
                  </FormItem>
                  <FormItem label="交易额">
                    <strong>0.00000000 USDT</strong>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Button type="primary" style="width:100%">买入</Button>
                  </FormItem>
                </Form>
              </Col>
              <Col span="12">
                <Form :label-width="50">
                  <FormItem label="卖出价">
                    <Input><span slot="append">USDT</span></Input>
                  </FormItem>
                  <FormItem label="卖出量">
                    <Input><span slot="append">&nbsp;IOTA&nbsp;</span></Input>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Slider v-model="sellAmtPercent" :tip-format="formatAmtPercent"></Slider>
                  </FormItem>

                  <FormItem label="交易额">
                    <strong>0.00000000 USDT</strong>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Button type="primary" style="width:100%">卖出</Button>
                  </FormItem>
                </Form>
              </Col>
            </Row>
          </TabPane>
          <TabPane label="市价交易" name="name2">
            <Row class="tx_opt_tab_row">
              <Col span="12">
                <Form :label-width="50">
                  <FormItem label="买入价">
                    <Input placeholder="以市场上最优价格买入" disabled>
                      <span slot="append">USDT</span>
                    </Input>
                  </FormItem>
                  <FormItem label="交易额">
                    <Input>
                      <span slot="append">&nbsp;IOTA&nbsp;</span>
                    </Input>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Slider v-model="buyaAmtPercent" :tip-format="formatAmtPercent"></Slider>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Button type="primary" style="width:100%">买入</Button>
                  </FormItem>
                </Form>
              </Col>
              <Col span="12">
                <Form :label-width="50">
                  <FormItem label="卖出价">
                    <Input placeholder="以市场上最优价格卖出" disabled>
                      <span slot="append">USDT</span>
                    </Input>
                  </FormItem>
                  <FormItem label="卖出量">
                    <Input><span slot="append">&nbsp;IOTA&nbsp;</span></Input>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Slider v-model="sellAmtPercent" :tip-format="formatAmtPercent"></Slider>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Button type="primary" style="width:100%">卖出</Button>
                  </FormItem>
                </Form>
              </Col>
            </Row>
          </TabPane>
          <TabPane label="止盈止损" name="name3">
            <Row class="tx_opt_tab_row">
              <Col span="12">
                <Form :label-width="50">
                  <FormItem label="触发价">
                    <Input>
                      <span slot="append">USDT</span>
                    </Input>
                  </FormItem>
                  <FormItem label="买入价">
                    <Input>
                      <span slot="append">USDT</span>
                    </Input>
                  </FormItem>
                  <FormItem label="买入量">
                    <Input>
                      <span slot="append">&nbsp;IOTA&nbsp;</span>
                    </Input>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Slider v-model="buyaAmtPercent" :tip-format="formatAmtPercent"></Slider>
                  </FormItem>
                  <FormItem label="交易额">
                    <strong>0.00000000 USDT</strong>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Button type="primary" style="width:100%">买入</Button>
                  </FormItem>
                </Form>
              </Col>
              <Col span="12">
                <Form :label-width="50">
                  <FormItem label="触发价">
                    <Input>
                      <span slot="append">USDT</span>
                    </Input>
                  </FormItem>
                  <FormItem label="卖出价">
                    <Input><span slot="append">USDT</span></Input>
                  </FormItem>
                  <FormItem label="卖出量">
                    <Input><span slot="append">&nbsp;IOTA&nbsp;</span></Input>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Slider v-model="sellAmtPercent" :tip-format="formatAmtPercent"></Slider>
                  </FormItem>

                  <FormItem label="交易额">
                    <strong>0.00000000 USDT</strong>
                  </FormItem>
                  <FormItem :label-width="0">
                    <Button type="primary" style="width:100%">卖出</Button>
                  </FormItem>
                </Form>
              </Col>
            </Row>
          </TabPane>
      </Tabs>
    </div>
</template>
<script>
export default {
  data() {
    return {
      buyaAmtPercent: 0,
      
      sellAmtPercent: 0
    };
  },
  methods: {
    formatAmtPercent(val){
      return val + "%";
    },
  }
};
</script>
<style>
.tx_container{
  height: 100%;
  width: 100%;
}
.tx_container .trading_market_card{
  width: 100%;
  height: calc(100% - 280px);
  margin-bottom: 5px;
}
.tx_container .trading_market_card .ivu-card-head{
  padding: 0 20px;
}
.tx_container .trading_market_card .ivu-card-head >div .ivu-row-flex{
  width: 100%;
  height: 45px;
}
.tx_container .trading_market_card .ivu-card-head .ivu-row-flex >div{
  margin-right: 15px;
}
.tx_container .trading_market_card .ivu-card-head .ivu-row-flex >div >span{
  display: block;
  font-size: 14px;
}
.tx_container .trading_market_card .ivu-card-head .symbol_name{
  font-size: 16px;
  font-weight: 550;
  margin-right: 20px !important;
}
.tx_container .trading_market_card_head .price_container >span:nth-of-type(1){
  font-size: 16px !important;
  color: #41b37d !important;
}
.tx_container .trading_market_card_head .price_container >span:nth-of-type(2){
  color: rgb(143, 150, 165);
}
.tx_container .trading_market_card_head .change >span:nth-of-type(1){
  color: rgb(143, 150, 165);
}
.tx_container .trading_market_card_head .change >span:nth-of-type(2){
  color: #41b37d !important;
}
.tx_container .trading_market_card_head .high >span:nth-of-type(1){
  color: rgb(143, 150, 165);
}
.tx_container .trading_market_card_head .low >span:nth-of-type(1){
  color: rgb(143, 150, 165);
}
.tx_container .trading_market_card_head .amount >span:nth-of-type(1){
  color: rgb(143, 150, 165);
}


.tx_container .tx_opt_tab{
  width: 100%;
  height: 275px;
  background: #ffffff;
}
.tx_container .tx_opt_tab .ivu-tabs-bar{
  margin-bottom: 10px;
}
.tx_container .tx_opt_tab .tx_opt_tab_row{
  width: 100%;
  height: 225px;
}
.tx_container .tx_opt_tab .tx_opt_tab_row .ivu-col{
  height: 225px;
  padding: 0 30px;
}
.tx_container .tx_opt_tab .tx_opt_tab_row .ivu-col:nth-of-type(1){
  border-right: 1px dashed #DCDEE2;
}
.tx_container .tx_opt_tab .tx_opt_tab_row .ivu-col .ivu-form-item{
  margin-bottom: 5px !important;
}
.tx_container .tx_opt_tab .tx_opt_tab_row .ivu-col .ivu-form-item input{
  z-index: 0;
}
</style>
