<template>
  <!-- Uses FlexBox -->
  <div class="tweet">
    <figure class="tweet-avatar">flexbox</figure>
    <div class="tweet-main">
      <div class="tweet-header">
        <div class="tweet-title">
          <div class="tweet-name">{{ projectInfo.name }}</div>
          <div class="tweet-username">{{ projectInfo.author }}</div>
          <time>{{ projectInfo.duration }}</time>
        </div>
        <div class="tweet-options">...</div>
      </div>
      <div class="tweet-body">
        <p class="tweet-content">
          {{ projectInfo.desc }}
        </p>
        <div class="tweet-actions">
          <button class="tweet-action">💬{{ projectInfo.flexibility }}</button>
          <button class="tweet-action">🔃{{ projectInfo.framework }}</button>
          <button class="tweet-action">❤️ {{ projectInfo.duration }}</button>
          <button class="tweet-action">📤{{ projectInfo.score }}</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FlexBox',
  props: {
    projectInfo: {
      type: Object,
      require: true,
    },
  },
};
</script>

<style lang="scss" scoped></style>
