<template>
  <div class="white-body-view">
    <div class="content-view">
      <div v-for="(item,index) in dataList" :id="'item' + index" :key="index" class="item">
        <span>item: {{ item.name }}</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dataList: [
        {
          name: '1'
        },
        {
          name: '2'
        },
        {
          name: '3'
        },
        {
          name: '4'
        },
        {
          name: '5'
        },
        {
          name: '6'
        },
        {
          name: '7'
        },
        {
          name: '8'
        },
        {
          name: '9'
        },
        {
          name: '10'
        },
        {
          name: '11'
        },
        {
          name: '12'
        }
      ]
    }
  },
  mounted() {
    document.getElementById('item5').scrollIntoView()
  }
}
</script>
<style lang="scss">
.content-view {
  height: 200px;
  width: 200px;
  overflow: auto;
}
.item {
  line-height: 40px;
}
</style>
