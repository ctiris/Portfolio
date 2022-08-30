<template>

  <div class="container is-fluid">
    <nav class="navbar is-fixed-top">
      <div class="container is-fluid">
        <div class="navbar-brand">
          <NuxtLink to="work" class="navbar-item">Iris Chang</NuxtLink>
        </div>
        <div class="navbar-menu">
          <div class="navbar-start">
              <NuxtLink to="/work" class="menu-link navbar-item">Work</NuxtLink>
              <NuxtLink to="/me" class="menu-link navbar-item">Me</NuxtLink>
              <NuxtLink to="/play" class="menu-link navbar-item">Play</NuxtLink>
          </div>
        </div>
      </div>
    </nav>



    <NuxtPage />
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


 
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap");




.menu-link {
  color: rgba(0, 0, 0, 0.5);
  margin-left: 35px;
  margin-right: 35px;
}

.menu-link:hover {
  color: black;
  transition: color 0.5s;
}

.router-link-active {
  font-family: 'Inter', sans-serif;
  color: black;
}


.navbar {
  display: flex;
  background-color: transparent;
  backdrop-filter: blur(10px);

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