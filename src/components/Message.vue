<template>
  <div class="WhatsappChat__MessageContainer-quaMo quaMo">
    <div
      style="opacity: 1"
      class="WhatsappChat__Message-sc-1wqac52-4 kAZgZq"
      v-for="(item, i) in messages"
      :key="i"
    >
      <div class="WhatsappChat__Author-sc-1wqac52-3 bMIBDo">
        {{ companyName }}
      </div>
      <div class="WhatsappChat__Text-sc-1wqac52-2 iSpIQi">
        {{ item }}
      </div>
      <div class="WhatsappChat__Time-sc-1wqac52-5 cqCDVm">
        {{ time }}
      </div>
    </div>
  </div>
</template>
<style>
.quaMo {
  z-index: 1;
}
.vzZsj {
  background-color: #fff;
  width: 52.5px;
  border-radius: 16px;
  display: flex;
  -moz-box-pack: center;
  justify-content: center;
  -moz-box-align: center;
  align-items: center;
  margin-left: 10px;
  opacity: 0;
  transition: all 0.1s ease 0s;
  z-index: 1;
  box-shadow: rgba(0, 0, 0, 0.13) 0px 1px 0.5px;
}
.Yvjha {
  position: relative;
  display: flex;
}
.ixsrax {
  height: 5px;
  width: 5px;
  margin: 0px 2px;
  border-radius: 50%;
  display: inline-block;
  position: relative;
  animation-duration: 1.2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  top: 0px;
  background-color: #9e9da2;
  animation-name: ZpjSY;
}
.dRvxoz {
  height: 5px;
  width: 5px;
  margin: 0px 2px;
  background-color: #b6b5ba;
  border-radius: 50%;
  display: inline-block;
  position: relative;
  animation-duration: 1.2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  top: 0px;
  animation-name: hPhMsj;
}
.kAZgZq {
  padding: 7px 14px 6px;
  background-color: #fff;
  border-radius: 0px 12px 12px;
  position: relative;
  transition: all 0.3s ease 0s;
  opacity: 0;
  transform-origin: center top 0px;
  z-index: 2;
  box-shadow: rgba(0, 0, 0, 0.13) 0px 1px 0.5px;
  margin-top: 20px;
  max-width: calc(100% - 66px);
}
.kAZgZq::before {
  position: absolute;
  background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAmCAMAAADp2asXAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAACQUExURUxpccPDw9ra2m9vbwAAAAAAADExMf///wAAABoaGk9PT7q6uqurqwsLCycnJz4+PtDQ0JycnIyMjPf3915eXvz8/E9PT/39/RMTE4CAgAAAAJqamv////////r6+u/v7yUlJeXl5f///5ycnOXl5XNzc/Hx8f///xUVFf///+zs7P///+bm5gAAAM7Ozv///2fVensAAAAvdFJOUwCow1cBCCnqAhNAnY0WIDW2f2/hSeo99g1lBYT87vDXG8/6d8oL4sgM5szrkgl660OiZwAAAHRJREFUKM/ty7cSggAABNFVUQFzwizmjPz/39k4YuFWtm55bw7eHR6ny63+alnswT3/rIDzUSC7CrAziPYCJCsB+gbVkgDtVIDh+DsE9OTBpCtAbSBAZSEQNgWIygJ0RgJMDWYNAdYbAeKtAHODlkHIv997AkLqIVOXVU84AAAAAElFTkSuQmCC');
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-size: contain;
  content: '';
  top: 0px;
  left: -12px;
  width: 12px;
  height: 19px;
}
.bMIBDo {
  font-size: 13px;
  font-weight: 700;
  line-height: 18px;
  text-align: left;
  color: rgba(0, 0, 0, 0.4);
}
.iSpIQi {
  font-size: 14px;
  line-height: 19px;
  margin-top: 4px;
  color: #111;
  text-align: left;
}
.cqCDVm {
  text-align: right;
  margin-top: 4px;
  font-size: 12px;
  line-height: 16px;
  color: rgba(17, 17, 17, 0.5);
  margin-right: -8px;
  margin-bottom: -4px;
}
</style>
<script>
export default {
  props: {
    messages: {
      type: Array,
      required: true,
    },
    companyName: {
      type: String,
      default: '',
    },
  },
  computed: {
    time() {
      return new Date().getHours() + ':' + new Date().getMinutes();
    },
  },
};
</script>
