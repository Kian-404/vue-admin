<template>
  <div class="clearfix">
    <div class="showAside pull-left" @click="toggleClick">
      <i class="el-icon-circle-plus" v-show="isCollapse"></i>
      <i class="el-icon-remove" v-show="!isCollapse"></i>
    </div>
  </div>
</template>
<script>
import {mapState} from 'vuex';
export default {
  name: "showAside",
  props: {
    toggleClick: {
      type: Function,
      default: null
    }
  },
  computed:{
    ...mapState(["isCollapse"])
  }
};
</script>
<style lang="scss" scoped>
.showAside {
  text-align: left;
  margin-left: 10px;
  cursor: pointer;
  i {
    font-size: 20px;
  }
}
</style>

