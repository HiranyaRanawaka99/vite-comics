<script>
  export default {
    data () {
      return {
        socialIcons: [
          {
            img: "src/assets/img/footer-facebook.png",
            url: "#asdsad",
            active: false,
          },
          {
            img: "src/assets/img/footer-periscope.png",
            url: "#",
            active: false,
          },
          {
            img: "src/assets/img/footer-pinterest.png",
            url: "#",
            active: false,
          },
          {
            img: "src/assets/img/footer-twitter.png",
            url: "#",
            active: false,
          },
          {
            img: "src/assets/img/footer-youtube.png",
            url: "#",
            active: false,
          },
        ],
      }
    },
  }
</script>


<template>

  <div class="footerBottom container">
      <button class="sign-up-btn">
        SIGN-UP NOW!
      </button>
    <div class="social">
      <p>FOLLOW US</p>
        <div 
          class="social-icons"
          v-for = "icon in socialIcons">
          <a :href="icon.url">
            <img :src="icon.img">
         </a>
        </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../assets/styles/general.scss' as *;

//   VARIABLES
  @use '../assets/styles/partials/variables' as *;

.footerBottom.container {
  display: flex;
  justify-content: space-between;

  padding-top: 2rem;
  padding-bottom: 2rem;

  background-color: $footer-color;

  .sign-up-btn {
    background-color:  $footer-color;
    color: $white-text;
    border: 2px solid $primary-color;
    padding: .5rem;

    &:hover {
      cursor: pointer;

    &:active {
      border: 3px solid $primary-color;
    }
    }
  }

  .social {
    display: flex;
    align-items: center;
    gap: .8rem;

    p {
      font-weight: 800;
      font-size: .8rem;
      color: $primary-color;
      &:hover {
      cursor: pointer;
      }
   }
  }
}

</style>