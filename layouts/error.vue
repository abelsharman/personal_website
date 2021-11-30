<template>
    <div class="error_layout" v-if="error.statusCode === 404" >
      <img src="~/assets/images/404.svg" alt="" />
      <p>The page does not exist or has been deleted</p>
      <nuxt-link to="/">Go back to the main page</nuxt-link>
    </div>    
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
};
</script>

<style scoped lang="scss">
.error_layout{
    height: 100vh;
    width: 100vw;
    background-color: rgb(28, 28, 30);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    img{
        width: 35vw;
    }
    p{
        color: #FFF;
        margin-top: 5vh;
        font-size: 1.4vw;
    }
    a{
        background-color: rgb(255, 69, 58);
        border-radius: 40px;
        padding: 1.7vh 5vw;
        color: #FFF;
        margin-top: 4vh;
        text-decoration: none;
        font-size: 1.5vw;
    }
}
@media screen and (max-width: 768px) {
    .error_layout{
        img{
            width: 75vw;
        }
        p{
            font-size: 3vw;
        }
        a{
            font-size: 3.2vw;
        }
    }
}
</style>
