<template>

  <div class="aside">
    <div class="aside__nav">
      <div class="aside__nav--back">
        <img src="~/assets/icons/arrow-back-outline.svg" alt="">
      </div>
      <div class="aside__nav--notification">
        <img src="~/assets/icons/notifications-outline.svg" alt="">
      </div>

    </div>
    <div class="aside__profile">
      <app-avatar size="230" source="https://images.unsplash.com/photo-1484186139897-d5fc6b908812?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"></app-avatar>
      <div class="profile-name">
        <h2>Amy</h2>
      </div>
    </div>

    <div class="aside__list">
      <ul>
        <li>Team <span>2</span></li>
        <li>Projects <span>6</span></li>
        <li>Feedback <span>12</span></li>
      </ul>
    </div>

    <div class="aside__action">
      <h2>Premium access</h2>
      <p>Create teams without limits</p>
      <button><a href="#">Get Premium Access</a></button>
    </div>

  </div>

  
</template>

<script>
import AppAvatar from '../components/ui/AppAvatar';
  export default {
    data(){
      return{
       
      }
    }
  }
</script>

<style lang="scss">
  .aside{
  background: $aside-color;
  padding: 3em 2em;
  @include large{
    grid-row: 1/3;
  }
  &__nav{
    width: 100%;
    @include flex-center-vert;
    justify-content: space-between;
  }

  &__profile{
    margin: 2.3em 0 0 1em;
    @include flex-center;
    flex-direction: column;

    .profile-name{
      margin-top: .5em;
    }
  }

  &__list{
    margin: 1.4em 0;
    font-size: 1.2rem;
    @include flex-column;

    li{
      position: relative;
      margin-right: auto;
      display: inline-block;
      width: 100%;
      padding: 1em 0;
      transition: all .5s ease;
      cursor: pointer;
      &:not(:last-child){
        border-bottom: 1px solid rgb(184, 183, 183);
      }
       

      span{
        position: absolute;
        right: 0;
      }

      &:hover{
        color: $hover-color;
      }
      
    }
    
  }

  &__action{
    width: 100%;
    padding: 2em;
    background: url('~assets/action-bg.jpg');
    background-position: top left;
    background-size: 100%;
    border-radius: 15px;
    text-align: center;
    @include large{
        padding: 1em ;
      }
    h2{
      font-size: 2rem;
      margin-bottom: .8rem;
    }

    p{
      margin-bottom: 1.5rem;
    }

    button{
      cursor: pointer;
      width: 100%;
      padding: 1em 2.5em;
      border-radius: 8px;
      background: $dune;
      transition: all .5s ease;
      border: none;
      outline: none;
      word-wrap: none;
      @include large{
        padding: 1em 1em;
      }
      a{
        
        font-weight: 600;
        color: $white;
      }

      &:hover{
        background: $hover-color;
      }
    }
    
    
  }
}


</style>