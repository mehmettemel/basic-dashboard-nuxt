<template>
  <div class="main">
    <main-header></main-header>
    <main-teams></main-teams>
    <main-projects></main-projects>
  </div>
</template>

<script>
import MainHeader from '../components/MainHeader'
import MainTeams from '../components/MainTeams'
import MainProjects from '../components/MainProjects'
  export default {
    components:{
      MainHeader,
      MainTeams,
      MainProjects
    }
  }
</script>

<style lang="scss" >
.main{
  background: $main-color;
  height: 100%;
  z-index: 2;
  padding: 2em;
  

  
  @include large{
    grid-row: 3 /4;
    width: 100%;
    display: flex;
    flex-basis: 100%;
    flex-direction: column;
  }
}
</style>