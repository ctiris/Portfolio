<template>

<link rel="stylesheet" href="https://use.typekit.net/qpz2fcw.css">
  <div>
    <div class="head-text-container">
      <p class="head-text">
        Hey there! I’m <a href=/me>
          <underline><bold>Iris Chang</bold></underline>
        </a>, an undergraduate student at <a href=/me>
          <underline>UCLA</underline></a>. I’m interested in <a href=#UXdesigns>
          <underline>UX
            design</underline>
        </a> and creating beautiful experiences.
      </p>

      <div class="scroll-down" id="section04">
        <a href="#UXdesigns"><span></span></a>
      </div>
    </div>
  </div>





  <div>
    <div id="UXdesigns">
      <div class="columns is-gapless is-multiline" id="blur">
        <div class="column is-one-third">
          <div class="card" id="first-card">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/artschoolsfbay.png" alt="Art School of SF Bay">
              </figure>
            </div>
            <div class="card-content">
              <div class="media">
                <div class="media-content">
                  <!-- <p class="subtitle is-6"><subtitle>DESIGN CATEGORY</subtitle></p> -->
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="column is-two-thirds">
          <div class="card">
            <div class="card-image">
              <figure class="image is-2by1">
                <img src="img/trek.png" alt="trek">
              </figure>
            </div>
            <div class="card-content">
              <div class="media">
                <div class="media-content">
                  <!-- <p class="subtitle is-6"><subtitle>DESIGN CATEGORY</subtitle></p> -->
                </div>
              </div>
            </div>
          </div>
        </div>


        <div class="column is-two-thirds">
          <div class="card">
            <div class="card-image">
              <figure class="image is-2by1">
                <img src="img/trek.png" alt="Art School of SF Bay">
              </figure>
            </div>
            <div class="card-content">
              <div class="media">
                <div class="media-content">
                  <!-- <p class="subtitle is-6"><subtitle>DESIGN CATEGORY</subtitle></p> -->
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="column is-one-third">
          <div class="card">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/artschoolsfbay.png" alt="trek">
              </figure>
            </div>
            <div class="card-content">
              <div class="media">
                <div class="media-content">
                  <!-- <p class="subtitle is-6"><subtitle>DESIGN CATEGORY</subtitle></p> -->
                </div>
              </div>
            </div>
          </div>
        </div>




      </div>

    </div>
  </div>
</template>

<script setup>
onMounted(() => {
  let blurMe = document.querySelector("#blur")

  let options = {
    threshold: new Array(101).fill().map((_, idx) => idx / 100)
  }

  let observer = new IntersectionObserver((entries) => {
    let intersectPercent = entries[0].intersectionRatio

    let blurRate = (1 - Math.min(intersectPercent, 1)) * 5
    blurMe.style["filter"] = `blur(${blurRate}rem)`
  }, options)

  observer.observe(document.querySelector("#first-card"))
})
</script>

<style>
html {
  scroll-behavior: smooth;
}


#section04 a span {
  position: absolute;
  top: 0;
  left: 50%;
  width: 24px;
  height: 24px;
  margin-left: -12px;
  border-left: 4px solid black;
  border-bottom: 4px solid black;
  -webkit-transform: rotate(-45deg);
  transform: rotate(-45deg);
  -webkit-animation: sdb04 2s infinite;
  animation: sdb04 2s infinite;
  box-sizing: border-box;
  
}




@-webkit-keyframes sdb04 {
  0% {
    -webkit-transform: rotate(-45deg) translate(0, 0);
  }

  20% {
    -webkit-transform: rotate(-45deg) translate(-10px, 10px);
  }

  40% {
    -webkit-transform: rotate(-45deg) translate(0, 0);
  }
}

@keyframes sdb04 {
  0% {
    transform: rotate(-45deg) translate(0, 0);
  }

  20% {
    transform: rotate(-45deg) translate(-10px, 10px);
  }

  40% {
    transform: rotate(-45deg) translate(0, 0);
  }
}


bold{
  font-weight: 500 !important;
}


.card {
  box-shadow: none;

}

.card-content {
  background-color: transparent;
  padding: 0rem !important;

}

.card-image:first-child img {
  border-top-left-radius: 0rem !important;
  border-top-right-radius: 0rem !important;
  border-bottom-left-radius: 0rem !important;
  border-bottom-right-radius: 0rem !important;
}

.head-text {

  padding: 34vh;

  font-family: 'rooney-web', serif;
  font-style: normal;
  font-weight: 400;
  font-size: 50px;
  line-height: 65px;
  text-align: left;
  /* letter-spacing: -0.03em; */
}


underline {
  color: black;
  text-decoration: underline;
  text-decoration-style: dotted;
  text-decoration-thickness: 2px;
  text-decoration-color: rgba(0, 0, 0, 0.15);
  text-underline-offset: 6px;
}

underline:hover {
  color: black;
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-decoration-color: black;
  text-underline-offset: 6px;
  transition: text-decoration-color 0.5s;
}


subtitle {
  font-family: 'Karla';
  font-style: normal;
  font-weight: 700;
  font-size: 12px;
  line-height: 38px;
  letter-spacing: 0.1em;
  color: black;
}

project-title {
  font-family: 'Karla';
  font-style: normal;
  font-weight: 600;
  font-size: 32px;
  line-height: 39px;
  letter-spacing: -0.03em;
  color: black;
}
</style>