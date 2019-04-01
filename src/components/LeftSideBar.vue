<template>
  <div class="left_sidr_bar_wrap">
    <section>

    </section>
    <section>

    </section>
    <section>
      <Table
        :columns="columns1"
        :data="data1"
      ></Table>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      columns1: [
        {
          title: "币种",
          key: "coin",
          sortable: true
        },
        {
          title: "最新价",
          key: "price",
          sortable: true
        },
        {
          title: "涨幅",
          key: "gain",
          sortable: true
        }
      ],
      data1: [
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
      ]
    };
  }
};
</script>

<style>
.left_sidr_bar_wrap {
  height: 100%;
  width: 100%;
}
</style>
