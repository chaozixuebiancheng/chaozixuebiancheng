<!-- 音量调节界面 -->
<script setup lang="ts">
import { MusicPlayer } from '@/hooks/interface'
const { setVolume, volume } = inject('MusicPlayer') as MusicPlayer
</script>
<template>
  <div class="flex items-center">
    <el-button text circle>
      <icon-bi:volume-up />
    </el-button>
    <!-- 这是一个滑动条 -->
    <el-slider v-model="volume" :show-tooltip="false" @change="setVolume" class="!w-24" size="small" />
  </div>
</template>
