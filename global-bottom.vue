<template>
  <div class="deck-page-number" aria-hidden="true">
    <span>{{ String($nav.currentPage).padStart(2, '0') }}</span>
  </div>
</template>

<style>
.deck-page-number {
  position: absolute;
  right: 76px;
  bottom: 43px;
  z-index: 20;
  display: flex;
  align-items: baseline;
  color: rgba(22, 21, 15, 0.68);
  font-family: var(--font-mono, monospace);
  font-size: 14px;
  font-weight: 800;
  letter-spacing: 0.02em;
  line-height: 1;
}

</style>
