<template>
  <div class="container">
    <div class="columns menu">
      <div class="column">
        <a href="/work">Iris Chang</a>
      </div>
      <div class="column menu-links">
        <a href="/work">Work</a>
        <a href="/me" id="me">Me</a>
        <a href="/play">Play</a>
      </div>
      <div class="column"></div>


      <!-- <div class="left">
        <a href="/work">Iris Chang</a>
      </div>

      <div class="center">
        <a href="/work">Work</a>
        <a href="/me">Me</a>
        <a href="/play">Play</a>
      </div>

      <div class="right"></div> -->
    </div>
    <NuxtPage />
  </div>
</template>

<style>
.menu {
  /* display: flex;
  flex-direction: row;
  justify-content: center; */
}

.menu-links {
  text-align: center;
  
}

#me {
  margin-left: 70px;
  margin-right: 70px;
}


</style>