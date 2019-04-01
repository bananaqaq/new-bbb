<template>
  <div class="quotes_container">
    <Row class="category_container" type="flex" justify="center">
      <RadioGroup v-model="category" type="button">
        <Radio label="自选"><Icon type="md-star" size="15" style="margin-top:-2px;"/>自选</Radio>
        <Radio label="USDT"></Radio>
        <Radio label="BTC"></Radio>
        <Radio label="ETH"></Radio>
      </RadioGroup>
    </Row>
    <Row class="search_container" type="flex" justify="space-between">
        <Input placeholder="搜索" style="width:210px;">
            <Icon type="ios-search" slot="prefix" />
        </Input>
        <Button type="primary" icon="md-swap">CNY</Button>
    </Row>
    <Row class="main_container">
      <Table
        :columns="quotesColumn"
        :data="quotesData"
        height="686"
        size="small"
      >
        <template slot-scope="{ row, index }" slot="coin">
            <Icon type="md-star" size="20" style="margin-top:-4px;"/>
            <strong>{{ row.coin }}</strong>
        </template>
      </Table>
    </Row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quotesColumn: [
        {
          title: "币种",
          slot: "coin",
          sortable: true,
          align: 'center'
        },
        {
          title: "最新价",
          key: "price",
          sortable: true,
          align: 'center'
        },
        {
          title: "涨幅",
          key: "gain",
          sortable: true,
          align: 'center'
        }
      ],
      quotesData: [
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
        {
          coin: "BTC",
          price: 18,
          gain: "5%"
        },
      ],
      category: "USDT"
    };
  }
};
</script>

<style>
.quotes_container {
  height: 100%;
  width: 100%;
}
.quotes_container .category_container{
  margin-top: 10px;
  margin-bottom: 10px;
}
.quotes_container .search_container{
  margin-bottom: 10px;
}
.quotes_container .main_container{
  width:100%;
}
.quotes_container .main_container table td{
  height:30px;
}
</style>
