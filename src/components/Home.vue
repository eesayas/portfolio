<template>
  <div class="home-cont">
    <div class="d-flex w-100">
    </div>
    <div id="text" class="mx-5">
      <p>My name is Isaias Briones III.</p>
      <p>I am a Full Stack, Mobile and Game Developer.</p>
    </div>
    <i class="material-icons bounce" role="button">expand_more</i>
  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .home-cont{
    position: relative;
    height: calc(100% - 6.3rem);
    margin-top: 6.3rem;
  }

  .home-cont > div{
    position: absolute;
  }

  img{
    opacity: 50%;
  }

  #text{
    font-size: 3rem;
    top: 30%;
  }

  .material-icons{
    position: absolute;
    width: 100%;
    font-size: 5rem;
    bottom: 0;
    text-align: center;
  }

  .bounce {
    -moz-animation: bounce 2s infinite;
    -webkit-animation: bounce 2s infinite;
    animation: bounce 2s infinite;
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
      transform: translateY(0);
    }
    40% {
      transform: translateY(-30px);
    }
    60% {
      transform: translateY(-15px);
    }
  }

</style>
