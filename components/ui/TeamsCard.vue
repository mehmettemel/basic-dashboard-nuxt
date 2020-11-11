<template>
  <div class="teams-card">
    <div class="attendees">
      <div class="avatars" v-for="attend in team.attendees" :key="attend.id">
         <app-avatar class="avatar" size="40" :source="attend.image"></app-avatar>
      </div>

       <img src="~/assets/icons/ellipsis-vertical-outline.svg" alt="">

    </div>
    <div class="info">
      <h2>{{team.title}}</h2>
      <h4>{{team.date}}</h4>
    </div>
  </div>
</template>

<script>
import AppAvatar from '../ui/AppAvatar';
  export default {
    props:{
      team:Object,
    },
    components:{
      AppAvatar
    }

    
  }
</script>

<style lang="scss" scoped>
.teams-card{
  padding: 1em 1.2em;
  width: 100%;
  margin-bottom: 1.5em;
  height: 200px;
  border-radius: 10px;
  background: white;
  transition: all .5s cubic-bezier(0.075, 0.82, 0.165, 1);
  &:hover{
    background: $hover-color;
    color: $white;
  }

  cursor: pointer;

  .attendees{
    @include flex-center-vert;
    img{
      margin-left: auto;
    }
    .avatars{
      &:not(:first-child){
        margin-left:.3em;
      }
    }
  }

  .info{
    margin-top: 2em;
    h4{
      margin-top: 1em;
      font-weight: 300;
    }
  }
}
</style>