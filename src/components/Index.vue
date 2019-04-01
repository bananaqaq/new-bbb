<template>
  <div class="layout">
    <Layout class="index_wrap">
      <Header class="bbb-header">
        <new-bbb-header />
      </Header>
      <Layout class="bbb-layout">
        <Sider class="left-side-bar">
          <left-side-bar />
        </Sider>
        <Content>
          <tx-content />
        </Content>
        <Sider class="right-side-bar-1">
          <right-side-bar-1 />
        </Sider>
        <Sider class="right-side-bar-2">
          <right-side-bar-2 />
        </Sider>
      </Layout>
      <Footer>
        <new-bbb-footer />
      </Footer>
    </Layout>
  </div>
</template>

<script>
import NewBBBHeader from "./NewBBBHeader";
import TxContent from "./TxContent";
import LeftSideBar from "./LeftSideBar";
import RightSideBar1 from "./RightSideBar1";
import RightSideBar2 from "./RightSideBar2";
import NewBBBFooter from "./NewBBBFooter";
export default {
  components: {
    "new-bbb-header": NewBBBHeader,
    "tx-content": TxContent,
    "left-side-bar": LeftSideBar,
    "right-side-bar-1": RightSideBar1,
    "right-side-bar-2": RightSideBar2,
    "new-bbb-footer": NewBBBFooter
  }
};
</script>

<style>
.index_wrap{
  height: 100%;
  min-width: 1350px;
}
.bbb-header{

}
.bbb-layout{
  height: 780px;
}
.left-side-bar{
  width: 300px !important;
  max-width: 300px !important;
  flex:0 0 300px !important;
  margin: 5px 5px 5px 0;
}
.right-side-bar-1{
  width: 300px !important;
  max-width: 300px !important;
  flex:0 0 300px !important;
  margin: 5px 0 5px 5px;
}
.right-side-bar-2{
  width: 300px !important;
  max-width: 300px !important;
  flex:0 0 300px !important;
  margin: 5px 0 5px 5px;
}
</style>
