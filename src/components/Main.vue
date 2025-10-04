<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Markdown from './sections/Markdown.vue'
import BibTeX from './sections/BibTeX.vue'
import Carousel from './sections/Carousel.vue'
import Video from './sections/Video.vue'

// benchmark statics method experiment demo

export default {
  components: {
    Title,
    Video,
    Abstract,
    Markdown,
    BibTeX
  }
}
</script>

<template>
  <Title/>
  <Video/>
  <Abstract/>
  <Markdown/>
  <BibTeX/>
</template>
