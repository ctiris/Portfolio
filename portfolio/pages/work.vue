<template>
  <div>
    <div class="head-text-container">
      <p class="head-text">
        Hey there! I’m <a href=/me><underline>Iris Chang</underline></a>, an undergraduate student at UCLA. I’m interested in <a href=/work><underline>UX
          design</underline></a> and creating subtle
        interfaces that are fun and spark joy.
      </p>
    </div>






    <div class="columns">
      <div class="column is-half">
        <div class="card">
          <div class="card-image">
            <figure class="image is-16by9">
              <img src= "img/artschoolsfbay.png" alt ="Art School of SF Bay">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
              <!-- <p class="subtitle is-6"><subtitle>DESIGN CATEGORY</subtitle></p> -->
                <p class="title is-4"><project-title>Project 1</project-title></p>
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
            <figure class="image is-16by9">
              <img src="img/trek.png" alt="trek">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <!-- <p class="subtitle is-6"><subtitle>DESIGN CATEGORY</subtitle></p> -->
                
                <p class="title is-4"><project-title>Project 2</project-title></p>
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




  </div>
</template>

<style>


        
.head-text {
  border-style: solid;
  border-width: 10px;
  border-color: black;
  padding: 20%;

  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-size: 28px;
  line-height: 38px;
  text-align: center;
  letter-spacing: -0.03em;
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