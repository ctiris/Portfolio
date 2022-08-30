<template>

  <div class="container is-fluid">
    <nav class="navbar is-fixed-top">
      <div class="container is-fluid">
        <div class="navbar-brand">
          <NuxtLink to="work" class="navbar-item">
            <top-logo>Iris Chang</top-logo>
          </NuxtLink>
        </div>
        <div class="navbar-menu">
          <div class="navbar-start">
            <NuxtLink to="/work" class="menu-link navbar-item">
              <top-link>Work</top-link>
            </NuxtLink>
            <NuxtLink to="/me" class="menu-link navbar-item">
              <top-link>Me</top-link>
            </NuxtLink>
            <NuxtLink to="/play" class="menu-link navbar-item">
              <top-link>Play</top-link>
            </NuxtLink>
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


.top-logo {
  color: black;
}


.top-logo:hover {
  color: orangered;
  transition: color 0.2s;
}

.top-link {
  color: rgba(0, 0, 0, 0.5);
  background: none;
}

.top-link:hover {
  color: orangered;
  background: none;
}



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
  background: none;
}


.navbar {
  display: flex;
  background-color: rgba(255, 255, 255, 0.5);
  border: 2px solid rgba(255, 255, 255, 0.15);
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


.footer{

padding-top: 6rem;
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