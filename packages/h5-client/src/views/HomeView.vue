<template>
  <main>
    <!-- <TheWelcome /> -->
    <el-btn msg="test" @confirm="confirmHandler"></el-btn>
  </main>
</template>

<script setup lang="ts">
// import TheWelcome from "@/components/TheWelcome.vue";
import { ElBtn } from "@elben/components";
import { getUserId } from "@elben/apis";
import { onMounted } from "vue";

onMounted(() => {
  console.log(getUserId(987123));
});

const confirmHandler = (msg) => {
  console.log(msg);
};
</script>
