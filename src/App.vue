<template>
  <div id="app">
    <div class="modules">
      <div class="module-item">
        <grid-box :projectInfo="projectB"></grid-box>
      </div>
      <div class="module-item">
        <flex-box :project-info="projectA"></flex-box>
      </div>
      <div class="module-item">
        <grid-box :project-info="projectB"></grid-box>
      </div>
      <div class="module-item">
        <flex-box :projectInfo="projectA"></flex-box>
      </div>
      <div class="module-item">
        <grid-box :project-info="projectB"></grid-box>
      </div>
    </div>
    <!-- <h1></h1>
    <h1>Cards for capturing recent work projects</h1>
    <p>🔊 From CodePen origin work: FlexBox vs Grid</p> -->
  </div>
</template>

<script>
import { projectA, projectB } from './data';
import FlexBox from './components/FlexBox.vue'
import GridBox from './components/GridBox.vue';

export default {
  name: 'App',
  components: {
    FlexBox,
    GridBox,
  },
  data:() => ({
    num: 100,
    projectA,
    projectB,
  }),
  created() {
    let vh = window.innerHeight * 0.01;
    document.documentElement.style.setProperty("--vh", `${vh}px`);

    window.addEventListener('resize', () => {
        let vh = window.innerHeight * 0.01;
        document.documentElement.style.setProperty("--vh", `${vh}px`);
    });
  }
}
</script>

<style lang="scss">
html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-image: url('data:image/svg+xml,%3Csvg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"%3E%3Cg fill-rule="evenodd"%3E%3Cg fill="%239C92AC" fill-opacity="0.4"%3E%3Cpath opacity=".5" d="M96 95h4v1h-4v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9zm-1 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm9-10v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm9-10v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm9-10v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9z"/%3E%3Cpath d="M6 5V0H5v5H0v1h5v94h1V6h94V5H6z"/%3E%3C/g%3E%3C/g%3E%3C/svg%3E');
}

*, *:before, *:after {
  box-sizing: border-box;
  position: relative;
}

.tweet,.tweet2 {
  padding: 1rem 1rem 0;
  border: 1px solid #aaa;
  margin-bottom: 1rem;
}

.tweet {
  outline: 1px solid;
  display: flex;
  flex-direction: row;
  width: fit-content;
  min-width: 40rem;
  padding: 1rem 1rem 0;
  background: #111821;
  color: white;
}

.tweet2 {
  width: fit-content;
  min-width: 40rem;
  display: grid;
  grid-template-columns: 5rem auto;
  grid-column-gap: 1rem;
  grid-template-rows: auto auto;
  grid-template-areas:
    'avatar header'
    'avatar content'
    'avatar actions';
  
  > .tweet-avatar {
    grid-area: avatar;
  }
  > .tweet-header {
    grid-area: header;
    justify-content: flex-start;
    align-items: center;
  }
  > .tweet-content {
    grid-area: content
  }
  > .tweet-actions {
    grid-area: actions;
  }
}

.tweet-avatar {
  flex-shrink: 0;
  flex-grow: 0;
  background: #fba31e;
  height: 5rem;
  width: 5rem;
  border-radius: 5rem;
  margin: 0;
  padding: 1rem;
}

.tweet-main {
  flex-grow: 1;
  margin-left: 1rem;
}

.tweet-header {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  gap: 1ch;
  
  > .tweet-options {
    margin-left: auto;
  }
}

.tweet-title {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 1ch;
}

.tweet-actions {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.tweet-action {
  padding: 1rem 0;
  appearance: none;
  border: none;
  background: none;
  color: white,
}

.tweet-name {
  font-weight: bold;
}

.tweet-content {
  margin: 0.25rem 0;
}
</style>
<style lang="scss">
@import url('./assets/style.css');
@import url('./assets/seasonal.css');
</style>