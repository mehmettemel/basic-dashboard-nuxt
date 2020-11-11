<template>
  <div class="projects-card">
    <div class="title">
      <div class="symbol">
        <img src="~/assets/icons/desktop-outline.svg" alt="" />
      </div>
      <h4>{{ project.title }}</h4>
    </div>
    <div class="attendees"></div>
    <div class="status">
      <div class="process" v-if="project.status === 'In Work'">In work</div>
      <div class="done" v-if="project.status === 'Published'">Published</div>
    </div>
    <div class="menu">
      <img src="~/assets/icons/ellipsis-horizontal-outline.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    project: Object
  }
};
</script>

<style lang="scss" scoped>
.projects-card {
  @include flex-center-vert;
  width: 100%;
  border-radius: 8px;
  padding: 1.5em;
  background: $white;
  margin-top: 1.5em;

  .menu {
    margin-left: auto;
  }

  .title {
    @include flex-center-vert;
    width: 30%;

    h4 {
      margin-left: 1.5em;
      font-weight: $font-regular;
    }
    .symbol {
      @include flex-center;
      border-radius: 10px;
      width: 70px;
      height: 50px;
      background: #faf3dd;
    }
  }

  .status {
    margin-left: auto;
    .process {
      color: red;
    }

    .done {
      color: $hover-color;
    }
  }
}
</style>
