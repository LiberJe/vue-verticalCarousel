# vue-verticalCarousel
一个简单的竖滑轮播组件

## 安装

`npm install -S vue-vertical-carousel`

## 参数

|参数|格式|备注|
|---|---|---|
|time|Int|轮播时间间隔，默认3000ms|
|loop|Boolean|是否循环，默认true|
|onSlidEnd|Function|每次轮播切换结束的回调函数|

## 用例

```
<template>
  <div>
    <Carousel>
      <!-- 注意这里一定要使用v-for语法,或不换行写入多个子元素。vue会将换行识别为一个'undefined'vnode -->
      <div v-for="(item,index) in arr" :key="index">{{item}}</div>
    </Carousel>
  </div>
</template>

<script>
import VerticalCarousel from "verticalCarousel"

export default {
  data () {
    return {
      arr: [1,2,3,4]
    }
  },
  components: {
    Carousel: VerticalCarousel,
  },
}
</script>
```
