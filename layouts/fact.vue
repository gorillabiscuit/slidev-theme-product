<!--
  fact layout — a single large number or statement, centered in the slide.
  Markup only. Vertical centering lives in styles/index.css
  (.slidev-layout.fact > div) using a scale-aware calc so it hits the true
  visual midpoint regardless of viewport size.
-->
<template>
  <div class="slidev-layout fact">
    <div>
      <slot />
    </div>
  </div>
</template>
