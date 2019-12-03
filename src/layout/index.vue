<template>
  <el-container>
    <el-aside>
      <siderbar />
    </el-aside>

    <el-main>
      <router-view :key="key" />
    </el-main>
  </el-container>
</template>

<script>
import Siderbar from "./components/Siderbar.vue";
export default {
  data() {
    return {};
  },
  computed: {
    key() {
      return this.$route.path
    }
  },
  components: {
    Siderbar
  }
};
</script>

<style lang="scss" scoped>
.el-container {
  height: 100%;
}
</style>