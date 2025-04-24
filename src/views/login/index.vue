<template>
  <div>
    <el-row>
      <el-col :span="12">
        <div class="grid-content ep-bg-purple" />
        <h1>hhh</h1>
      </el-col>
      <el-col :span="12">
        <div class="grid-content ep-bg-purple-light" />
        <h1>hhh</h1>
        <el-button type="primary" @click="onRegister">注册</el-button>
        <!-- <el-button type="primary" @click="onLogin">登录</el-button> -->
      </el-col>
    </el-row>
  </div>
</template>

<script setup lang="ts">
import { getRegister } from "@/api/user";
import { ElMessage } from "element-plus";

defineOptions({
  name: "index"
});

const onRegister = async () => {
  try {
    const res = await getRegister({
      username: "shimily",
      password: "000000"
    });
    ElMessage.success(res);
  } catch (error) {
    console.error(error);
  }
};
</script>

<style lang="scss" scoped>
// 样式之后添加
</style>
