<template>
  <div class="teams">
    <div class="teams__header">
      <h2>Teams</h2>
      <a href="#">View all</a>
    </div>
    <div class="teams__main">
      <teams-card 
      v-for="team in teams" 
      :key="team.id"
      :team="team">
      </teams-card>
    </div>
  </div>
</template>

<script>
import TeamsCard from '../components/ui/TeamsCard';
  export default {
    data(){
      return{
      "teams": [ 
    {
      "id": 5928101,
      "title": "Product Presentation",
      "date": "05 May , 2020",
      "attendees":[
        {
         "id": "312",
        "image": "https://images.unsplash.com/photo-1485528562718-2ae1c8419ae2?ixlib=rb-1.2.1&auto=format&fit=crop&w=781&q=80"
        },
        {
         "id": "abc121323123",
        "image": "https://images.unsplash.com/photo-1529068755536-a5ade0dcb4e8?ixlib=rb-1.2.1&auto=format&fit=crop&w=801&q=80"
        },
      ],
     
    },
     {
      "id": 5928102,
      "title": "New Project",
      "date": "15 Jun, 2020",

      "attendees":[
        {
         "id": "abc123",
        "image": "https://images.unsplash.com/photo-1527980965255-d3b416303d12?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"
        },
      ],
     
    },
     {
      "id": 5928103,
      "title": "Design Development",
      "date": "02 Feb, 2020",

      "attendees":[
        {
         "id": "abc12322",
        "image": "https://images.unsplash.com/photo-1485206283729-2ca7d035185e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"
        },
        {
         "id": "abc123321312",
        "image": "https://images.unsplash.com/photo-1499887142886-791eca5918cd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"
        },
      ],
     
    },
      
        ]
    }
    },
    components:{
      TeamsCard
    }
  }
</script>

<style lang="scss" scoped>
.teams{
  margin-top: 3.5em;
  &__header{
    @include flex-center-vert;
    justify-content: space-between;
    

  
    h2{
      font-size: 2rem;
    }
    a{
      color: black;
      line-height: 33px;
      transition: all .5s ease;
      cursor: pointer;

      &:hover{
        color: $hover-color;
      }
    }
  }

  &__main{
    margin-top: 1.5em;
    width: 100%;
    height: 100%;
    display: grid;
    grid-template-columns: repeat( auto-fit, minmax(290px, 1fr));
    place-items: center;
    gap: 1em;
    
  }
}
</style>