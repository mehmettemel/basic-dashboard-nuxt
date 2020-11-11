<template>
  <div class="projects">
    <div class="projects__header">
      <h2>Projects</h2>
      <div class="projects__header--action">
        <div class="filter">
          <img src="~/assets/icons/filter-outline.svg" alt="" />
        </div>
        <div class="add">
          <img src="~/assets/icons/add-outline.svg" alt="" />
        </div>
      </div>
    </div>
    <div class="project__main">
      <project-card
        v-for="project in projects"
        :key="project"
        :project="project"
      >
      </project-card>
    </div>
  </div>
</template>

<script>
import ProjectCard from "../components/ui/ProjectsCard";
export default {
  components: {
    ProjectCard
  },
  data() {
    return {
      projects: [
        {
          id: 3213,
          title: "Product Presentation",
          date: "12 February , 2020",
          status: "Published",
          attendees: [
            {
              id: "312",
              image:
                "https://images.unsplash.com/photo-1485528562718-2ae1c8419ae2?ixlib=rb-1.2.1&auto=format&fit=crop&w=781&q=80"
            },
            {
              id: "abc121323123",
              image:
                "https://images.unsplash.com/photo-1529068755536-a5ade0dcb4e8?ixlib=rb-1.2.1&auto=format&fit=crop&w=801&q=80"
            }
          ]
        },
        {
          id: 5435,
          title: "Healthy Lifestyle",
          date: "31 November, 2020",
          status: "Published",

          attendees: [
            {
              id: "abc123",
              image:
                "https://images.unsplash.com/photo-1527980965255-d3b416303d12?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"
            }
          ]
        },
        {
          id: 4232,
          title: "Design Development",
          date: "02 April, 2020",
          status: "In Work",

          attendees: [
            {
              id: "abc12322",
              image:
                "https://images.unsplash.com/photo-1485206283729-2ca7d035185e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"
            },
            {
              id: "abc123321312",
              image:
                "https://images.unsplash.com/photo-1499887142886-791eca5918cd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=80"
            }
          ]
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.projects {
  margin-top: 2em;
  margin-bottom: 2em;
  &__header {
    @include flex-center-vert;
    h2 {
      font-size: 2rem;
    }

    &--action {
      margin-left: auto;
      @include flex-center-vert;
      .filter,
      .add {
        @include flex-center;
        width: 90px;
        height: 50px;
        border-radius: 10px;
        transition: all 0.5s ease;
        cursor: pointer;
        &:hover {
          background: $hover-color;
        }
      }
      .filter {
        background: white;
        margin-right: 2rem;
      }
      .add {
        background: $dune;
      }
    }
  }
}
</style>
