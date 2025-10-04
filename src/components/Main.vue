<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Benchmark from './sections/benchmark.vue'
import Mcg from './sections/mcg.vue'
import Experiment from './sections/experiment.vue'
import BibTeX from './sections/BibTeX.vue'
import Carousel from './sections/Carousel.vue'
import Video from './sections/Video.vue'

// benchmark statics method experiment demo

export default {
  components: {
    Title,
    Video,
    Abstract,
    Benchmark,
    Mcg,
    Experiment,
    BibTeX
  }
}
</script>

<template>
  <Title/>
  <Video/>
  <Abstract/>
  <Benchmark/>
  <Mcg/>
  <Experiment/>
  <BibTeX/>
</template>
