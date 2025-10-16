<script setup>
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Explainer Video</h1>
    </el-row>

    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="14" :xl="12">
        
        <!-- 本地视频版本 -->
        <el-container class="video-container">
          <video 
            controls
            autoplay
            muted
            loop
          >
            <source src="/videos/demo.mp4" type="video/mp4">
            Your browser does not support the video tag.
          </video>
        </el-container>

      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.video-container {
  margin: 20px 0px 0px 0px;
}

video {
  aspect-ratio: 16 / 9;
  width: 100%;
  border-radius: 8px;
  background: black;
}
</style>
