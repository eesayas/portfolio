<template>
  <div>
    <img
      src="https://media.licdn.com/dms/image/v2/C5603AQG8oikx_4bm_w/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646460298961?e=1741219200&v=beta&t=qwJJRDiuRRbyLQx8kKxKyyAlLU0FnhNDzR15cqJHDjo"
      class="rounded-circle mb-4"
      height="150"
    />

    <h1>
      My name is <br />
      Isaias Briones
    </h1>
    <p>
      I am an experienced Full-Stack, Mobile, and Software Engineer. I love
      watching movies, playing music, and coding.
    </p>
    <a
      class="d-flex align-items-center"
      role="button"
      target="_blank"
      href="mailto:briones@ualberta.ca"
    >
      <font-awesome-icon :icon="['fas', 'envelope']" size="lg" />
      <span class="mx-2">briones@ualberta.ca</span>
    </a>
    <a
      class="d-flex align-items-center mt-1"
      role="button"
      target="_blank"
      href="sms:+1-780-278-6076"
    >
      <font-awesome-icon :icon="['fas', 'phone']" size="lg" />
      <span class="mx-2">1 (780) 278 6076</span>
    </a>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
div {
  width: 500px;
}

h1 {
  font-family: RubikMedium;
  font-size: 4rem;
  line-height: 0.9;
}
p {
  font-family: RubikLight;
  color: #939393;
  width: 400px;
  font-size: 1.1rem;
}

@media screen and (max-width: 1250px) {
  h1 {
    font-size: 3rem;
  }
}

@media screen and (max-width: 562px) {
  div {
    width: auto;
  }
}

@media screen and (max-width: 460px) {
  p {
    width: auto;
  }
}
</style>
