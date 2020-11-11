<template>
  <div class="navbar">
    <div class="navbar__main">
      <ul>
        <li><img src="~/assets/icons/home-outline.svg" alt="" /></li>
        <li><img src="~/assets/icons/bar-chart-outline.svg" alt="" /></li>
        <li><img src="~/assets/icons/star-outline.svg" alt="" /></li>
        <li><img src="~/assets/icons/chatbox-outline.svg" alt="" /></li>
        <li><img src="~/assets/icons/albums-outline.svg" alt="" /></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.navbar {
  z-index: 3;
  height: 100%;
  background: $main-color;
  grid-column: 1/2;
  @include flex-center;

  @include large {
    position: fixed;
    height: 10px;
    bottom: 0;
    width: 100%;
    order: 3;
  }

  &__main {
    border-radius: 15px;
    padding: 2.7em 1em;
    background: white;
    box-shadow: rgba(17, 17, 26, 0.1) 0px 8px 24px,
      rgba(17, 17, 26, 0.1) 0px 16px 56px, rgba(17, 17, 26, 0.1) 0px 24px 80px;
    @include large {
      width: 100%;
      padding: 0;
      padding-bottom: 2em;
    }

    ul {
      @include flex-column;
      @include large {
        align-items: center;
        justify-content: center;
        flex-direction: row;
      }

      li {
        position: relative;
        padding: 0.2em;
        cursor: pointer;
        margin: 1em 0;
        border-radius: 5px;
        transition: all 0.5s ease;

        &::after {
          @include pseudo;
          bottom: 0;
          left: 0;
          background: $hover-color;
          width: 0%;
          height: 3px;
          transition: all 0.7s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        &:hover::after {
          width: 100%;
        }

        @include large {
          padding: 0 2em;
        }
        @include phone {
          padding: 0 0.7em;
        }
      }
    }
  }
}
</style>
