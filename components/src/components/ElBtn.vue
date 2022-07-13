<template>
  <div class="btn" @click="click">
    {{ msg }}
  </div>
</template>

<script setup lang='ts'>
const props = defineProps<{
  msg: string
}>()

const emits = defineEmits<{
  // confrim: () => void
  (e: 'confirm', msg: string): void
}>()

const click =  () => {
  emits('confirm', 'emits params')
}
</script>

<style scoped>
.btn { 
  width: 200px;
  height: 40px;
  font-size: 16px;
  text-align: center;
  line-height: 40px;
  background: #abcdef;
  color: #333;
  border-radius: 6px;
}
</style>
