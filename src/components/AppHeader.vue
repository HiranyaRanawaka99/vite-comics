<script>
  export default {
    data () {
      return {
        image: "../../public/img/dc-logo.png",
        links: [
          {
            text: "CHARACTERS",
            url: "#",
            current: false,
          },
          {
            text: "COMICS",
            url: "#",
            current: false,
          },
          {
            text: "MOVIES",
            url: "#",
            current: false,
          },
          {
            text: "TV",
            url: "#",
            current: false,
          },
          {
            text: "GAMES",
            url: "#",
            current: false,
          },
          {
            text: "COLLECTIBLES",
            url: "#",
            current: false,
          },
          {
            text: "VIDEOS",
            url: "#",
            current: false,
          },
          {
            text: "FANS",
            url: "#",
            current: false,
          },
          {
            text: "NEWS",
            url: "#",
            current: false,
          },
          {
            text: "SHOP",
            url: "#",
            current: false,
          },
        ],
      }
    },
  }
</script>


<template>
    <div class="header container">
      <div class="div-logo">
        <img src="../assets/img/dc-logo.png" alt="DC-logo">
      </div>
        <ul>
          <li  v-for = "link in links">
            <a :href="link.url">
              {{ link.text }}
            </a>
          </li>
        </ul>
    </div>
 
</template>


<style lang="scss" scoped>
// GENERAL STYLE
  @use '../assets/styles/general.scss' as *;
//   VARIABLES
  @use '../assets/styles/partials/variables' as *;

.header.container  {
  display: flex;
  justify-content: space-between;
  align-items: center;

  height: 100px;
  padding-top: 2rem;
  padding-bottom: 2rem;


  .div-logo {
    width: 80px;
    height: 80px;
  }

  ul {
    min-height: 100%;

  }
  
  li {
    display: inline-block;
    height: 100%;

        font-weight: 800;
        padding: 2rem 1rem;

        a {
          display: inline-block;
          color: black;
          height: 100%;

          &:hover {
            border-bottom: 2px solid $primary-color;
          }
  
        }
      }
   }
  

</style>