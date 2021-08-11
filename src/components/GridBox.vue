<template>
  <!-- Uses CSS Grid: less nesting! -->
  <div class="tweet2">
    <figure class="tweet-avatar">Grid</figure>
    <div class="tweet-header">
      <div class="tweet-name">{{ projectInfo.name }}</div>
      <div class="tweet-username">{{ projectInfo.author }}</div>
      <time>{{ projectInfo.duration }}</time>
      <div class="tweet-options">...</div>
    </div>

    <p class="tweet-content">
      {{ projectInfo.desc }}
    </p>
    <div class="tweet-actions">
      <button class="tweet-action">💬</button>
      <button class="tweet-action">🔃</button>
      <button class="tweet-action">❤️ 12</button>
      <button class="tweet-action">📤</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GridBox',
  props: {
    projectInfo: {
      type: Object,
      require: true
    }
  }
};
</script>

<style lang="scss" scoped></style>
