<template>

  <link rel="stylesheet" href="https://use.typekit.net/qpz2fcw.css">
  <div>
    <div class="head-text-container">
      <p class="head-text">
        Hey there! I’m <a href=/me>
          <underline>
            <bold>Iris Chang</bold>
          </underline>
        </a>, an undergraduate student at <a href="projects/artschoolsfbay">
          <underline>
            <bold>UCLA</bold>
          </underline>
        </a>. I’m interested in <a href=#UXdesigns>
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
          <div class="card" id="first-card" style=" padding-right: 5px; padding-bottom: 5px;">
            <div class="card-image">
              <figure class="image is-1by1">


                <img src="img/artschoolsfbay.png" alt="Art School of SF Bay">


                <div class="overlay-bg"> </div>
                <div class="overlay-text">
                  <div class="text">
                    ART SCHOOL OF SF BAY
                    <br>

                    <div style=" font-size: 18px; font-weight: 400; color: #BFBFBF; letter-spacing: 0em"> UI/UX Design</div>

                  </div>
                </div>



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
          <div class="card" style=" padding-left: 5px; padding-bottom: 5px;">
            <div class="card-image">
              <figure class="image is-2by1">
                <img src="img/trek.png" alt="trek">

                <div class="overlay-bg"> </div>
                <div class="overlay-text">
                  <div class="text">
                    TREK
                    <br>

                    <div style=" font-size: 18px; font-weight: 400; color: #BFBFBF; letter-spacing: 0em"> UI/UX Design</div>


                  </div>
                </div>
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
          <div class="card" style=" padding-right: 5px; padding-top: 5px;">
            <div class="card-image">
              <figure class="image is-2by1">
                <img src="img/trek.png" alt="Art School of SF Bay">

                <div class="overlay-bg"> </div>
                <div class="overlay-text">
                  <div class="text">
                    ART SCHOOL OF SF BAY
                    <br>

                    <div style=" font-size: 18px; font-weight: 400; color: #BFBFBF; letter-spacing: 0em"> UI/UX Design</div>

                  </div>
                </div>
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
          <div class="card" style=" padding-left: 5px; padding-top: 5px;">
            <div class="card-image">
              <figure class="image is-1by1">
                <img src="img/artschoolsfbay.png" alt="trek">

                <div class="overlay-bg"> </div>
                <div class="overlay-text">
                  <div class="text">
                    PERSONAL PROJECTS
                    <br>
                    <div style=" font-size: 18px; font-weight: 400; color: #BFBFBF; letter-spacing: 0em"> Over here!</div>

                  </div>
                </div>
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
html {
  scroll-behavior: smooth;
}


#section04 {
  padding-bottom: 15vh;
}

#section04 a span {

  position: absolute;
  top: 1;
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


.overlay-bg {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .5s ease;
  background-color: black;
}

.card-image:first-child:hover .overlay-bg {
  opacity: .75;
}


.overlay-bg {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .3s ease;
  background-color: black;
}

.card-image:first-child:hover .overlay-bg {
  opacity: .75;
}

.overlay-text {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .3s ease;

}



.card-image:first-child:hover .overlay-text {
  opacity: 1;
}

.card-image:first-child:hover .text {
  opacity: 1;
}

.text {

  font-family: 'Karla';
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 38px;
  letter-spacing: 0.08em;


  color: white;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}

.caption {
  font-size: 18px !important;
}

bold {
  font-weight: 500 !important;
}


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
  box-shadow: none !important;
}

.head-text {

  padding: 28vh !important;

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