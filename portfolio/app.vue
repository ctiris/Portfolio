
<template>
  <link rel="stylesheet" href="https://use.typekit.net/qpz2fcw.css">
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
              <top-link>WORK</top-link>
            </NuxtLink>
            <NuxtLink to="/me" class="menu-link navbar-item">
              <top-link>ABOUT</top-link>
            </NuxtLink>
            <NuxtLink to="/play" class="menu-link navbar-item">
              <top-link>PLAY</top-link>
            </NuxtLink>
          </div>
        </div>
      </div>
    </nav>



    <NuxtPage />
    <footer class="footer">


      <div class="content has-text-centered">
        <p>
          <footer-size>
            Designed and coded on <a href="https://github.com/ctiris">
              <underline>ctiris</underline>
            </a> / 
            <a href="iristchang@g.ucla.edu">
              <underline>iristchang@g.ucla.edu</underline>
            </a> /
            <a href="https://jgthms.com">
              <underline>LinkedIn</underline>
            </a> /
            <a href="https://twitter.com/isEatingEggTart">
              <underline>Twitter</underline>
            </a> /
            <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
              <underline>Behance</underline>
            </a>.
          </footer-size>
        </p>
      </div>
    </footer>



    <!-- <div style="padding-top: 10000px"></div> -->

  </div>
</template>

<style>
/* inter */
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap");

/* karla */

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Karla:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,200;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');




footer-size {
  font-family: 'Karla', sans-serif;
  font-size: 18px;
  font-weight: 400;
  line-height: 17px;
  /* letter-spacing: -0.05em; */

}

top-logo {
  color: black;
}


top-logo:hover {
  color: orangered !important;
  transition: color 0.2s;
}



.menu-link {
  color: rgba(0, 0, 0, 0.5);
  margin-left: 35px;
  margin-right: 35px;
}

.menu-link:hover {
  color: black !important;
  background-color: transparent !important;
  transition: color 0.5s;
}

.router-link-active {
  color: black !important;
  background: none !important;
}


.navbar {
  display: flex;
  background-color: transparent;
  /* background-color: rgba(255, 255, 255, 0.5); */
  /* border: 2px solid rgba(255, 255, 255, 0.15); */
  backdrop-filter: blur(10px);

}

.navbar-start {
  flex-grow: 1;
  justify-content: right;
  font-family: 'Karla', sans-serif;
  font-size: 14px;
  font-weight: 500;
  line-height: 17px;
  letter-spacing: 0.05em;

}

.navbar-brand {
  position: fixed;
  font-family: 'Karla', sans-serif;
  font-size: 20px;
  font-weight: 700;
  line-height: 19px;
  /* letter-spacing: -0.05em; */
}


.content {
  font-family: 'Karla';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 30px;
  /* letter-spacing: -0.005em; */
  color: rgba(0, 0, 0, 0.5);
}




.footer {
  padding-top: 6rem;
  background: none;


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