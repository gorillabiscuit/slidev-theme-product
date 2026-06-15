<!--
  image-right layout — content on the left half, full-bleed image on the right.
  Two-column grid that fills the slide. `height: 100%` (NOT 100vh) so the
  image half matches the slide height in dev and export.

  Frontmatter:
    layout: image-right
    image: /path/or/url
    backgroundSize: cover   # optional, defaults to cover
    class: my-class         # optional, applied to the content column
-->
<script setup>
const props = defineProps({
  image: String,
  class: String,
  backgroundSize: { type: String, default: 'cover' },
})
</script>

<template>
  <div :style="{ display: 'grid', gridTemplateColumns: '1fr 1fr', width: '100%', height: '100%', boxSizing: 'border-box' }">
    <div class="slidev-layout default" :class="props.class">
      <slot />
    </div>
    <div :style="{ width: '100%', height: '100%', backgroundImage: image ? `url('${image}')` : 'none', backgroundSize: backgroundSize, backgroundPosition: 'center', backgroundRepeat: 'no-repeat' }" />
  </div>
</template>
