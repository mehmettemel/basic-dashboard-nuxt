<template>
  <div class="main-header">
    <div class="search-input">
      <button><img src="~/assets/icons/search-outline.svg" alt=""></button>
      <input type="text" placeholder="Project Search" autofocus>
    </div>
    <div class="user-profile">
        <span>Amy</span>
       <app-avatar size="55" source="https://images.unsplash.com/photo-1484186139897-d5fc6b908812?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"></app-avatar>
    </div>
  </div>
</template>

<script>
import AppAvatar from '../components/ui/AppAvatar';
  export default {
    components:{
      AppAvatar
    }
  }
</script>

<style lang="scss" scoped>
.main-header{
  @include flex-center-vert;
  width: 100%;
  justify-content: space-between;

  .search-input{
    border: 1px solid transparent;
    border-radius: 10px;
    width: 350px;
    background: white;
    padding: .5em;
    @include flex-center-vert;
   

    button{
      @include flex-center-vert;
      background: none;
      border: none;
      cursor: pointer;
    }

    input{
      border: none;
      outline: none;
      padding: .5em;
      width: 100%;
      background: none;
    }
  }

  .user-profile{
     @include flex-center-vert;
     span{
       margin-right: 1em;
       transition: all .5s ease;
      cursor: pointer;
       &:hover{
         color: $hover-color;
       }
     }
  }

}
</style>