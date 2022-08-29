<template>

  <div class="container is-fluid">
    <nav class="navbar is-fixed-top">
      <div class="container is-fluid">
        <div class="navbar-brand">
          Iris Chang
        </div>
        <div class="navbar-menu">
          <div class="navbar-start">
              <NuxtLink to="/work">Work</NuxtLink>
            <div class="center">
                <NuxtLink to="/me">Me</NuxtLink>
            </div>
              <NuxtLink to="/play">Play</NuxtLink>
          </div>
        </div>
      </div>
    </nav>


    <div class="columns">
      <div class="column is-half">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <p class="subtitle is-6">DESIGN CATEGORY</p>
                <p class="title is-4">Project 1</p>
              </div>
            </div>
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Phasellus nec iaculis mauris.
              <br>
            </div>
          </div>
        </div>
      </div>
      <div class="column is-half">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <p class="subtitle is-6">DESIGN CATEGORY</p>
                <p class="title is-4">Project 2</p>
              </div>
            </div>
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Phasellus nec iaculis mauris.
              <br>
            </div>
          </div>
        </div>
      </div>
    </div>


    <div class="columns">
      <div class="column is-half">

        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <p class="subtitle is-6">DESIGN CATEGORY</p>
                <p class="title is-4">Project 3</p>
              </div>
            </div>
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Phasellus nec iaculis mauris.
              <br>
            </div>
          </div>
        </div>
      </div>
      <div class="column is-half">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <p class="subtitle is-6">DESIGN CATEGORY</p>
                <p class="title is-4">Project 4</p>
              </div>
            </div>
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Phasellus nec iaculis mauris.
              <br>
            </div>
          </div>
        </div>
      </div>
    </div>


    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          <a href="iristchang@g.ucla.edu">iristchang@g.ucla.edu</a>
          <a href="https://jgthms.com">LinkedIn</a>
          <a href="https://twitter.com/isEatingEggTart">Twitter</a>
          <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Behance</a>.
        </p>
      </div>
    </footer>


    <NuxtPage />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap");

.nuxt-link-active {
  font-family: 'Inter', sans-serif;
  font-weight: bold;
  color: red;
}


.navbar {
  display: flex;
  background-color: transparent;
  backdrop-filter: blur(10px);
  padding-top: 0.6rem;
}

.navbar-start {
  flex-grow: 1;
  justify-content: center;
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 500;
  line-height: 17px;
  letter-spacing: -0.05em;

}

.center {
  padding-left: 60px;
  padding-right: 60px;
}

.navbar-brand {
  position: fixed;
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-weight: 700;
  line-height: 19px;
  letter-spacing: -0.05em;
}

.is-4 {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 32px;
  line-height: 39px;
  letter-spacing: -0.03em;
}


.is-6 {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 500;
  font-size: 8px;
  line-height: 38px;
  letter-spacing: 0.05em;
}


.content {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 30px;
  letter-spacing: -0.005em;
  color: rgba(0, 0, 0, 0.5);
}


#me {
  margin-left: 70px;
  margin-right: 70px;
}
</style>


<script setup>
useHead({
  title: 'Iris Chang',
  bodyAttrs: {
    class: 'has-navbar-fixed-top'
  }
})
</script>