<template>
  <div class="consult-fast-page">
    <cp-nav-bar title="极速问诊" right-text="问诊记录" />
    <div class="fast-logo">
      <img class="img" src="@/assets/consult-fast.png" alt="" />
      <p class="text"><span>20s</span>快匹配专业医生</p>
    </div>
    <div class="fast-type">
      <router-link
        to="/consult/dep"
        @click="store.setIllnessType(1)"
        class="item"
      >
        <cp-icon class="pic" name="consult-doctor"></cp-icon>
        <div class="info">
          <p>三甲图文问诊</p>
          <p>三甲主治及以上级别医生</p>
        </div>
        <van-icon name="arrow" />
      </router-link>
      <router-link
        to="/consult/dep"
        @click="store.setIllnessType(0)"
        class="item"
      >
        <cp-icon class="pic" name="consult-message"></cp-icon>
        <div class="info">
          <p>普通图文问诊</p>
          <p>二甲主治及以上级别医生</p>
        </div>
        <van-icon name="arrow"></van-icon>
      </router-link>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useConsultStore } from '@/stores';
const store = useConsultStore()
</script>

<style lang="scss" scoped>
.consult-fast-page {
  padding-top: 46px;
  .fast-logo {
    padding: 30px 0;
    text-align: center;
    .img {
      width: 240px;
    }
    .text {
      font-size: 16px;
      margin-top: 10px;
      > span {
        color: var(--cp-primary);
      }
    }
  }
  .fast-type {
    padding: 15px;
    .item {
      display: flex;
      padding: 16px;
      border-radius: 4px;
      align-items: center;
      margin-bottom: 16px;
      border: 0.5px solid var(--cp-line);
    }
    .info {
      margin-left: 12px;
      flex: 1;
    }
  }
}
</style>
