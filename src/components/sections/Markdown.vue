<script setup>
import page from '../mds/md.mdx';
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="16" :lg="16" :xl="16">
            <page />
        </el-col>
    </el-row>

  </div>
</template>
