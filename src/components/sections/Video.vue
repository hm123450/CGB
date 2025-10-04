<script setup>
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Explainer Video</h1>
    </el-row>

    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="16" :xl="12" >
        
        <!-- YouTube 版本 -->
        <el-container class="video-container">
          <iframe 
            src="https://www.youtube.com/embed/wjZofJX0v4M?si=BFvRyc3n3fFV_f1G" 
            frameborder="0" 
            allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
            referrerpolicy="strict-origin-when-cross-origin" 
            allowfullscreen>
          </iframe>
        </el-container>

      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.video-container {
  margin: 20px 0px 0px 0px;
}

iframe, video {
  aspect-ratio: 16 / 9;
  width: 100%;
}
</style>
