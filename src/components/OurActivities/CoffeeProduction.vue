<template>
  <div>
    <!-- Coffee Process -->
    <p>
      Our coffee is processed using a method known as wet processing. This
      removes the coffee's fruity material and leaves the coffee cherry
      moist.<br />
      It is passed through a pulping machine, fermented and dried using forced
      air drying to achieve a moisture content of about 10.5%.
    </p>
    <div class="flex-container">
      <div class="coffee-process-left">
        <!-- Coffee Process -->
        <carousel-3d>
          <slide class="slide" :index="0">
            <img src="../../../backend/uploads/mother-garden.jpg" />
            <br />
            <h4>1-Mother Garden</h4>
            <p>
              We have all 7 lines of coffee wilt disease resistant varieties and
              the traditional clones.
            </p>
          </slide>
          <slide class="slide" :index="2">
            <img src="../../../backend/uploads/cherry-picking.jpg" />
            <br />
            <h4>2-Cherry Picking</h4>
            <p>
              We have all 7 lines of coffee wilt disease resistant varieties and
              the traditional clones.
            </p>
          </slide>
          <slide class="slide" :index="1">
            <img src="../../../backend/uploads/wet-processing.jpg" />
            <br />
            <h4>3-Wet Processing</h4>
            <p>
              We have all 7 lines of coffee wilt disease resistant varieties and
              the traditional clones.
            </p>
          </slide>
        </carousel-3d>
      </div>

      <div class="coffee-benefits-right">
        <!-- Process Benefits -->
        <carousel-3d>
          <slide class="slide" :index="0">
            <br />
            <h4>01-Clean Taste</h4>
            <p>
              Our process guarantees a cleaner and more consistent flavor than
              other methods.
            </p>
          </slide>
          <slide class="slide" :index="2">
            <br />
            <h4>02-Selective Picking</h4>
            <p>
              Only the ripest green cherries are picked for processing. This
              guarantees a higher acidity and gives a better taste.
            </p>
          </slide>
          <slide class="slide" :index="1">
            <br />
            <h4>03-Quality Control</h4>
            <p>
              It guarantees a great deal of quality control through selective
              picking and allows for a much more consistent flavor.
            </p>
          </slide>
        </carousel-3d>
      </div>
    </div>
    <br />
    <!--Our Capacity-->
    <h3>Our Capacity</h3>
    <div class="capacity-section">
      <p>These statistics show our current production and growth potential.</p>
      <div>
        <div id="stat-container">
          <div class="stat">
            <div class="stat-num">1500</div>
            <div class="stat-text">Acres available</div>
          </div>
          <div class="stat">
            <div class="stat-num">300+</div>
            <div class="stat-text">Acres of coffee</div>
          </div>
          <div class="stat">
            <div class="stat-num">700K</div>
            <div class="stat-text">Kilograms annually</div>
          </div>
          <div class="stat">
            <div class="stat-num">50</div>
            <div class="stat-text">Employees</div>
          </div>
          <div class="stat">
            <div class="stat-num">300</div>
            <div class="stat-text">Seasonal workers</div>
          </div>
        </div>
      </div>
    </div>
    <br />
    <!--Our Partners-->
    <h3>Our Partners</h3>
    <br />
    <div id="our-partners">
      <div id="partners-container">
        <div class="partner">
          <img
            src="../../../backend/uploads/ucda.jpg"
            alt="Uganda Coffee Development Authority"
            aria-hidden="true"
          />
        </div>
        <div class="partner">
          <img
            src="../../../backend/uploads/ugacof.jpg"
            alt="UGACOF"
            aria-hidden="true"
          />
        </div>
        <div class="partner">
          <img
            src="../../../backend/uploads/great.jpg"
            alt="Great lakes coffee"
            aria-hidden="true"
          />
        </div>
        <div class="partner">
          <img
            src="../../../backend/uploads/lifad.jpg"
            alt="LIFAD"
            aria-hidden="true"
          />
        </div>
        <div class="partner">
          <img
            src="../../../backend/uploads/nucafe.png"
            alt="NUCAFE"
            aria-hidden="true"
          />
        </div>
      </div>
    </div>
    <br />
  </div>
</template>

<style scoped>
.slide {
  border: none;
  background-color: #f5f5f5;
}

h4 {
  text-align: center;
}

p {
  font-size: 13pt;
  text-align: center;
  margin-left: 5px;
  margin-right: 5px;
}

.coffee-process-left,
.coffee-benefits-right {
  /*padding: 10px;*/
  flex: 50%;
}

/* Capacity styles */
#stat-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 70%;
  margin-left: auto;
  margin-right: auto;
}

@media screen and (max-width: 480px) {
  #stat-container {
    width: 80%;
  }
}

.stat {
  margin-top: 20px;
  min-width: 100px;
  text-align: center;
}

@media screen and (max-width: 480px) {
  .stat {
    text-align: left;
  }
}

.stat-num {
  font-size: 45px;
  margin-top: -10px;
  color: rgb(100, 100, 100);
  font-family: "Times New Roman", Times, serif;
}

@media screen and (max-width: 764px) {
  #our-partners {
    margin-top: 30px;
  }
}

#partners-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 95%;
  margin-left: auto;
  margin-right: auto;
  overflow-y: hidden;
  overflow-x: auto;
}

#partners-container::-webkit-scrollbar {
  width: 0px;
}

@media screen and (max-width: 630px) {
  #partners-container {
    margin-top: 40px;
  }
}

@media screen and (max-width: 1280px) {
  #our-partner {
    min-width: 100%;
  }
}

.partner {
  min-width: 200px;
  height: 100px;
  display: flex;
  align-items: center;
}

img {
  max-width: 100%;
  min-width: 100%;
  max-height: 100%;
  object-fit: contain;
}
</style>
