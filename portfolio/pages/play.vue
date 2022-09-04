<template>
  <link rel="stylesheet" href="https://use.typekit.net/qpz2fcw.css">
  <div>
    <div class="head-text-container">
      <p class="head-text">
        Hey there! I’m <a href=/me>
          <underline>book pageee</underline>
        </a>, an undergraduate student at UCLA. I’m interested in <a href=/work>
          <underline>UX
            design</underline>
        </a> and creating subtle
        interfaces that are fun and spark joy.
      </p>
    </div>
  </div>


  <div>

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
      <div class="column is-one-third">
        <div class="card">
          <div class="card-image">
            <figure class="image is-1by1">
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



      <div class="column is-one-third">
        <div class="card">
          <div class="card-image">
            <figure class="image is-1by1">
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

      <div class="column is-one-third">
        <div class="card">
          <div class="card-image">
            <figure class="image is-1by1">
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
</template>
  
  <script setup>
onMounted(() => {
  let blurMe = document.querySelector("#blur")

  let options = {
    threshold: new Array(101).fill().map((_, idx) => idx / 100)
  }

  let observer = new IntersectionObserver((entries) => {
    let intersectPercent = entries[0].intersectionRatio

    let blurRate = (1 - Math.min(intersectPercent, 1)) * 5.7
    blurMe.style["filter"] = `blur(${blurRate}rem)`
  }, options)

  observer.observe(document.querySelector("#first-card"))
})
</script>
  
  <style>
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
  
    padding: 33vh;
  
    font-family: 'rooney-web', serif;
    font-style: normal;
    font-weight: 400;
    font-size: 50px;
    line-height: 65px;
    text-align: left;
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
    font-family: 'Inter';
    font-style: normal;
    font-weight: 700;
    font-size: 12px;
    line-height: 38px;
    letter-spacing: 0.1em;
    color: black;
  }
  
  project-title {
    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 32px;
    line-height: 39px;
    letter-spacing: -0.03em;
    color: black;
  }
  </style>