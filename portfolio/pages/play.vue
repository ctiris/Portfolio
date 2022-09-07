<template>
  <link rel="stylesheet" href="https://use.typekit.net/qpz2fcw.css">
  <div>
    <div class="head-text-container">
      <p class="head-text">
        Outside of work, I'm also passionate about the creative and playful side of design
      </p>

      <div class="scroll-down" id="section04">
        <a href="#play"><span></span></a>
      </div>
    </div>
  </div>


  <div>
    <div id="play">
      <div class="columns is-gapless is-multiline" id="blur">
        <div class="column is-one-third">
          <div class="card" id="first-card" style=" padding-right: 5px; padding-bottom: 10px;">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/pin.jpg" alt="Art School of SF Bay">
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
          <div class="card" style=" padding-left: 5px; padding-right: 5px; padding-bottom: 10px;">
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
          <div class="card" style=" padding-left: 5px;  padding-bottom: 10px;">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/pin.jpg" alt="Art School of SF Bay">
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
          <div class="card" style=" padding-right: 5px; padding-bottom: 10px;">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/dream.png" alt="trek">
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
          <div class="card" style=" padding-left: 5px; padding-right: 5px; padding-bottom: 10px;">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/nostalgia.png" alt="trek">
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
          <div class="card" style=" padding-left: 5px; padding-bottom: 10px;">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/blocks.png" alt="trek">
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
// passes blur function to onMounted
onMounted(() => {

// gets a reference to part of html that we want to blur
let blurMe = document.querySelector("#blur")

// creates an object that holds the options for making IntersectionObserver
let options = {
  // creates array to hold all values from 0 - 1
  threshold: new Array(101).fill().map((_, idx) => idx / 100)
}

// creates a new IntersectionObserver 
let observer = new IntersectionObserver((entries) => { // passes in below function
  // prints out y values
  // console.log(entries[0].intersectionRect.y)
  // stops blur when card is going up off the screen
  if(entries[0].intersectionRect.y == 0) {
    return
  }

  // gets the IntersectionRatio from IntersectionObserver
  let intersectPercent = entries[0].intersectionRatio

  // when intersectPercent is off screen -> blurRate is 0, fully on screen -> blurRate is 5
  // Math.min truncates intersectPercent at 1
  let blurRate = (1 - Math.min(intersectPercent, 1)) * 5

  // applies blurRate to blur filter
  blurMe.style["filter"] = `blur(${blurRate}rem)`
}, options)

// calling observe function inside observer, takes a reference to the first card
observer.observe(document.querySelector("#first-card"))
})

</script>
  
  <style>
  .card {
    box-shadow: none !important;
    background-color: none !important;
  
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
  
    padding: 28vh;
  
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