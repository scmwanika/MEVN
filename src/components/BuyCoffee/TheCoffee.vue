<template>
  <div>
    <!--Coffee Process-->
    <h3>Coffee Process</h3>
  </div>
  <div class="flex-container">
    <div class="flex-item-left">
      <img
        src="../../../backend/uploads/mother-garden.jpg"
        alt="mother garden"
        width="100%"
      />
      <h4>1-Mother Garden</h4>
      <p>
        Our mother garden consists of a variety of coffee seedlings. We have all
        7 lines of coffee wilt disease resistant varieties and the traditional
        clones A-F.
      </p>
    </div>
    <div class="flex-item-middle">
      <img
        src="../../../backend/uploads/cherry-picking.jpg"
        alt="cherry picking"
        width="100%"
      />
      <h4>2-Cherry Picking</h4>
      <p>
        Our mother garden consists of a variety of coffee seedlings. We have all
        7 lines of coffee wilt disease resistant varieties and the traditional
        clones A-F.
      </p>
    </div>
    <div class="flex-item-right">
      <img
        src="../../../backend/uploads/wet-processing.jpg"
        alt="wet processing"
        width="100%"
      />
      <h4>3-Wet Processing</h4>
      <p>
        Our mother garden consists of a variety of coffee seedlings. We have all
        7 lines of coffee wilt disease resistant varieties and the traditional
        clones A-F.
      </p>
    </div>
  </div>
  <br /><br />
  <!--Process Benefits-->
  <h3 style="margin-right: 50%">Process Benefits</h3>
  <div class="flex-container">
    <div class="flex-item-left">
      <h4>☆ Clean Taste</h4>
      <p>
        Our process guarantees a cleaner and more consistent flavor than other
        methods.
      </p>
    </div>
    <div class="flex-item-middle">
      <h4>☆ Selective Picking</h4>
      <p>
        Only the ripest green cherries are picked for processing. This
        guarantees a higher acidity and gives a better taste.
      </p>
    </div>
    <div class="flex-item-right">
      <h4>☆ Quality Control</h4>
      <p>
        It guarantees a great deal of quality control through selective picking
        and allows for a much more consistent flavor.
      </p>
    </div>
  </div>
  <br /><br />
  <!--Our Capacity-->
  <h3 style="margin-left: 50%">Our Capacity</h3>
  <div class="capacity-section">
    <p style="text-align: right">These statistics show our current production and growth potential.</p>
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
  <br /><br /><br />
  <!--Our Partners-->
  <h3 style="margin-right: 50%">Our Partners</h3>
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
</template>

<style scoped>
h4 {
  text-align: center;
}

p {
  margin-left: 5%;
  margin-right: 5%;
  font-size: 14pt;
  text-align: justify;
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
