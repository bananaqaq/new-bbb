<template>
  <div class="order_container">
    <Card style="width:100%" dis-hover>
      <p slot="title">
        <!-- <Icon type="ios-film-outline"></Icon> -->
        盘口
      </p>
      <Table
        :columns="orderColumn"
        :data="orderData"
        size="small"
        height="333"
      >
      </Table>
      <Row
        type="flex"
        justify="space-between"
        class="tx_info"
      >
        <span>0.314<em> ≈ 2.14CNY</em></span>
        <span>
          <a href="https://www.google.com/">更多</a>
        </span>
      </Row>
      <Table
        :columns="orderColumn"
        :data="orderData"
        size="small"
        height="300"
        :show-header=false
      >
      </Table>
      <Row
        type="flex"
        justify="space-between"
        align="middle"
        class="setting_container"
      >
        <div class="buy_and_sell_container">
            <div>
                <img src="../assets/buy&sell.svg" />
            </div>
            <div>
                <img src="../assets/buy.svg" />
            </div>
            <div>
                <img src="../assets/sell.svg" />
            </div>
        </div>
        <Select
          v-model="pricePrecision"
          size="small"
          style="width:80px"
        >
          <Option
            v-for="pp in pricePrecisionList"
            :value="pp.value"
            :key="pp.value"
          >{{ pp.label }}</Option>
        </Select>
      </Row>
    </Card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      orderColumn: [
        {
          title: "价格(USDT)",
          key: "price",
          width: 100
        },
        {
          title: "数量(IOTA)",
          key: "amt",
          align: "right"
        },
        {
          title: "累计(IOTA)",
          key: "iota",
          align: "right"
        }
      ],
      orderData: [
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        },
        {
          price: 10,
          amt: 100,
          iota: 1000
        }
      ],
      pricePrecision: "4f",
      pricePrecisionList: [
        {
          value: "4f",
          label: "4位小数"
        },
        {
          value: "3f",
          label: "3位小数"
        },
        {
          value: "2f",
          label: "2位小数"
        },
        {
          value: "1f",
          label: "1位小数"
        },
        {
          value: "2d",
          label: "2位整数"
        },
        {
          value: "1d",
          label: "1位整数"
        }
      ]
    };
  }
};
</script>

<style>
.order_container {
  height: 100%;
  width: 100%;
}
.order_container .ivu-card-body {
  padding: 0 !important;
}
.order_container .ivu-card-body table td {
  height: 20px;
}
.order_container .tx_info span:nth-of-type(1) {
  font-size: 16px;
  color: #41b37d;
  padding: 15px 10px;
}
.order_container .tx_info span:nth-of-type(1) em {
  font-size: 14px;
  color: #515a6e;
}
.order_container .tx_info span:nth-of-type(2) {
  padding: 15px 10px;
}
.order_container .setting_container{
  height: 41px;
  padding-right: 10px;
  padding-left: 10px;
}
.order_container .setting_container .buy_and_sell_container{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.order_container .setting_container .buy_and_sell_container div{
    margin-right: 5px;
    width: 20px;
    height: 20px;
    border: 1px solid #a5a8af;
    border-radius:5px;
    text-align: center;
}
.order_container .setting_container .buy_and_sell_container div:hover{
    cursor: pointer;
    border: 1px solid #2D8CF0;
    border-radius:5px;
}
</style>
