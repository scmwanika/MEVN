<template>
  <div>
    <router-view />
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}

.navbar {
  width: 100%;
  position: fixed;
  top: 0px;
}

.content {
  display: flex;
  flex-direction: row;
  font-size: 20px;
}

.content-left {
  flex: 39%;
}

.content-middle {
  flex: 45%;
  text-align: center;
  background-color: #f5f5f5;
}

.hero {
  color: grey;
}

.content-right {
  flex: 16%;
}

.founder {
  display: flex;
  flex-direction: row;
  font-size: 20px;
}

.founder-left {
  flex: 33.33%;
}

.founder-right {
  flex: 66.66%;
  text-align: center;
  background-color: #f5f5f5;
}

p {
  margin-left: 2.5%;
  margin-right: 2.5%;
  font-size: 16pt;
  text-align: justify;
}

h2 {
  color: #068d68;
  text-align: center;
}

h3 {
  color: white;
  margin-left: 50%;
  font-size: 18pt;
  text-align: center;
  background-color: #068d68;
}

h4 {
  color: #068d68;
}

h5 {
  margin-left: 2.5%;
  margin-right: 2.5%;
  font-size: 16pt;
  text-align: justify;
}

.nav-header {
  margin-left: 2.5%;
}

.btn-outline-info {
  margin-left: 5px;
}

.flex-container {
  display: flex;
  flex-direction: row;
  font-size: 30px;
  text-align: center;
}

.about-investment-left,
.about-investment-middle,
.about-investment-right {
  /*padding: 10px;*/
  flex: 33.33%;
}

figure {
  margin-left: 2.5%;
  margin-right: 2.5%;
}

iframe {
  width: 100%;
  height: auto;
  border: none;
}

figcaption {
  text-align: center;
}

#app-footer {
  background-color: #068d68;
}

.footer {
  display: flex;
  flex-direction: row;
  font-size: 10pt;
  text-align: left;
}

.footer-item-left {
  background-color: white;
  text-align: center;
  flex: 33.33%;
}

.footer-item-middle,
.footer-item-right {
  background-color: #068d68;
  color: white;
  text-align: center;
  flex: 33.33%;
}

.copyright {
  text-align: center;
}

/* Responsive layout */
@media (max-width: 800px) {
  .content,
  .founder,
  .flex-container,
  .footer {
    flex-direction: column;
  }
}
</style>
