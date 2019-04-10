<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <img
          class="item-img"
          :src="item.imgUrl"
          alt=""
        >
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>

      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1903/de/de2b990eb2690294a3.img.jpg_200x200_b71c02ea.jpg',
          title: 'happy乐园',
          desc: '在这里玩转乐园，疯玩起来，无忧无虑一整天！'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
          title: '南昌必游TOP10',
          desc: '看山看水，看看历史对南昌的浸润'
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/df/9bcc134d126bc4.jpg_r_640x214_58a1f389.jpg',
          title: '陶醉青山绿水',
          desc:
            '一年四季景色秀丽，层峦叠嶂，岩石高高耸立，白雾弥漫，犹如人间仙境'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top 0.2rem
  line-height 0.8rem
  text-indent 0.2rem
  background #eee
.item
  display flex
  overflow hidden
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding 0.1rem
  .item-info
    flex 1
    padding 0.1rem
    min-width 0
    .item-title
      line-height 0.54rem
      font-size 0.32rem
      ellipsis()
    .item-desc
      line-height 0.4rem
      color #ccc
      ellipsis()
    .item-button
      background #ff9300
      margin-top 0.16rem
      color #fff
      border-radius 0.06rem
      padding 0 0.2rem
      line-height 0.44rem
</style>
