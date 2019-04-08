<template>

  <div class="real_time_tx_container">

    <Card style="width:100%" dis-hover>
      <p slot="title">
        实时成交
      </p>
      <Table
        :columns="rttxColumn"
        :data="rttxData"
        size="small"
        height="728"
      >
      </Table>
    </Card>
  </div>

</template>
<script>
export default {
  data() {
    return {
      rttxColumn: [
        {
          title: "时间",
          key: "time"
        },
        {
          title: "价格(USDT)",
          key: "price",
          align: "right",
          width: 101
        },
        {
          title: "数量(IOTA)",
          key: "amt",
          align: "right",
          width: 96
        }
      ],
      rttxData: [
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
        {
          time: "17:35:15",
          price: "100",
          amt: "10"
        },
      ]
    };
  }
};
</script>
<style>
.real_time_tx_container {
  height: 100%;
  width: 100%;
}
.real_time_tx_container .ivu-card-body {
  padding: 0 !important;
}
.real_time_tx_container .ivu-card-body table td {
  height: 20px;
}
</style>
