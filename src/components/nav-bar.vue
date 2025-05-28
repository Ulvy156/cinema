<template>
  <header class=" w-full p-4 text-white">
    <nav class=" w-[70%] m-auto">
      <section class="flex items-center justify-between gap-x-5 border-b border-[var(--bg-color)] pb-5">
        <el-input
          v-model="searchValue"
          style="width: 20%"
          size="large"
          placeholder="Please Input"
          :suffix-icon="Search"
        />
        <section class="flex items-center gap-x-5">
          <img src="../assets/img/legend-cinema-logo.png" alt="" />
          <div class="flex items-center gap-x-2 border border-white rounded-full p-1 px-4">
            <el-icon color="white"><Ticket /></el-icon>
            <p>Ticket</p>
          </div>
          <div class="flex items-center gap-x-2 border border-white rounded-full p-1 px-4">
            <el-icon color="white"><UserFilled /></el-icon>
            <p>Ticket</p>
          </div>
          <div class="flex items-center gap-x-2 border border-white rounded-full p-2">
            <el-icon color="white"><MuteNotification /></el-icon>
          </div>
          <el-dropdown placement="bottom-end">
            <el-button> bottomEnd </el-button>
            <template #dropdown>
              <el-dropdown-menu>
                <el-dropdown-item>The Action 1st</el-dropdown-item>
                <el-dropdown-item>The Action 2st</el-dropdown-item>
                <el-dropdown-item>The Action 3st</el-dropdown-item>
              </el-dropdown-menu>
            </template>
          </el-dropdown>
        </section>
      </section>
      <section class="flex items-center gap-x-10 mt-4">
        <div class="flex items-center gap-x-2">
          <el-icon color="red"><HomeFilled /></el-icon>
          Home
        </div>
        <div class="flex items-center gap-x-2">
          <el-icon color="white"><Location /></el-icon>
          Cinema
        </div>
        <div class="flex items-center gap-x-2">
          <el-icon color="white"><ShoppingCartFull /></el-icon>
          Offers
        </div>
        <div class="flex items-center gap-x-2">
          <el-icon color="white"><IceDrink /></el-icon>
          F&B
        </div>
      </section>
    </nav>
  </header>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import {
  Search,
  Ticket,
  UserFilled,
  MuteNotification,
  HomeFilled,
  Location,
  ShoppingCartFull,
  IceDrink,
} from '@element-plus/icons-vue'
const searchValue = ref<string>('')
</script>

<style></style>
