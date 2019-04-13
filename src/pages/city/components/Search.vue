<template>
  <div class="search">
    <input
      class="search-input"
      type="text"
      placeholder="输入城市名或拼音"
    >
  </div>

</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '~styles/variable.styl'
.search
  height 0.72rem
  background-color $bgColor
  padding 0 0.1rem
  .search-input
    box-sizing border-box
    height 0.62rem
    width 100%
    line-height 0.62rem
    text-align center
    border-radius 0.08rem
    color #666
    padding 0 0.1rem
</style>
