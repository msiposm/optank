<template>
  <div class="main">

    <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark navbar-custom">
      <div class="container-fluid">
        <a class="navbar-brand" v-on:click="section = 'main'">~/Michael_Sipos</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item header-item-text">
              <a class="nav-link" aria-current="page" v-on:click="section = 'main'">Home</a>
              <!-- <a class="nav-link active" aria-current="page" href="#">Home</a> -->
            </li>
            <li class="nav-item header-item-text">
              <a class="nav-link" v-on:click="section = 'experience'">Experience</a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                Projects
              </a>
              <ul class="dropdown-menu" aria-labelledby="navbarDropdown" style="background-color:black">
                <li><a class="dropdown-item" v-on:click="section = 'website'">Website</a></li>
                <li><a class="dropdown-item" v-on:click="section = 'projects'">Project 2</a></li>
                <!--<li><hr class="dropdown-divider"></li>-->
                <li><a class="dropdown-item" v-on:click="section = 'projects'">Project 3</a></li>
              </ul>
            </li>
            <!--
            <li class="nav-item header-item-text">
              <a class="nav-link" v-on:click="section = 'contact'">Contact</a>
            </li>
            <li class="nav-item">
              <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Projects <i>(coming soon)</i></a>
            </li>
            -->
          </ul>
        </div>
      </div>
    </nav>

    <div class="main-body">
      <div v-if="section == 'main' || section == 'about-me'" class="page-section">
        <h1>About Me</h1>
        <div class="panel-body">
          <p>My name is Michael</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Gravida rutrum quisque non tellus orci ac auctor. Enim diam vulputate ut pharetra sit amet aliquam id. Volutpat lacus laoreet non curabitur gravida arcu ac tortor dignissim. Convallis posuere morbi leo urna molestie at elementum eu. Amet purus gravida quis blandit turpis cursus in hac. Pellentesque elit eget gravida cum sociis natoque. Nunc aliquet bibendum enim facilisis gravida neque convallis a cras. Est sit amet facilisis magna etiam tempor orci. Nunc consequat interdum varius sit amet mattis. Mi sit amet mauris commodo quis imperdiet massa tincidunt nunc. Sit amet est placerat in egestas erat imperdiet sed. Pretium nibh ipsum consequat nisl vel pretium. Ac turpis egestas sed tempus urna et pharetra pharetra. Consequat mauris nunc congue nisi vitae.</p>
        </div>
      </div>

      <div v-if="section == 'experience'" class="page-section">
        <h1>Experience</h1>
        <div class="panel-body">
          <p>This section is currently under work. Please visit again soon!</p>
        </div>
      </div>

      <div v-if="section == 'website'" class="page-section">
        <h1>Website</h1>
        <div class="panel-body">
          <p>What you're looking at now!</p>
          <p>This website was hand-developed with custom HTML/CSS/JS built on a MEVN full-stack web development framework</p>
          <table style="margin-bottom:20px; margin-left:20px; font-family:'Inconsolata',monospace;">
            <tr>
              <td>MongoDB</td>
              <td>NoSQL database</td>
            </tr>
            <tr>
              <td>Express.js</td>
              <td>Web framework</td>
            </tr>
            <tr>
              <td>Vue.js</td>
              <td>Front-end/UI framework</td>
            </tr>
            <tr>
              <td>Node.js</td>
              <td>JavaScript runtime environment</td>
            </tr>
          </table>
          <p>Hosting is provided via Amazon Web Services (AWS) with website code residing on GitHub. A Test / Build / Deploy process is implemented via cloud CI/CD technologies on AWS. With a simple GitHub push, the pipeline is automatically triggered!</p>
          <p>Additional libraries and tools used:</p>
          <table style="margin-bottom:20px; margin-left:20px; font-family:'Inconsolata',monospace;">
            <tr>
              <td>Babel</td>
              <td>JavaScript transcompiler</td>
            </tr>
            <tr>
              <td>Eslint</td>
              <td>JavaScript code linter</td>
            </tr>
            <tr>
              <td>Webpack</td>
              <td>Code bundler</td>
            </tr>
            <tr>
              <td>Axios</td>
              <td>HTTP client</td>
            </tr>
            <tr>
              <td>Bootstrap</td>
              <td>UI library</td>
            </tr>
            <tr>
              <td>Nodemon</td>
              <td>Hot reload for development</td>
            </tr>
            <tr>
              <td>Mongoose</td>
              <td>Object modeller for MongoDB</td>
            </tr>
          </table>
        </div>
      </div>

      <div v-if="section == 'projects'" class="page-section">
        <h1>Projects</h1>
        <div class="panel-body">
          <p>Additional projects coming soon!</p>
        </div>
      </div>
      <hr />
      <p class = "footer-text">
        Copyright &#169; 2021 Michael Sipos. All Rights Reserved
    </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      section: 'main'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.header-menu {
  background: black;
  padding-left: 10%;
  padding-right: 10%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.navbar-custom {
  font-family: "Open Sans", sans-serif;
  background-color: rgb(0, 0, 0) !important;
}

.navbar-brand {
  font-family: 'Inconsolata', monospace;
  color: white;
  cursor: pointer;
  font-size: 32px;
}

.nav-item {
  color: rgb(136, 136, 136);
  cursor: pointer;
  font-family: 'Raleway', sans-serif;
  font-size: 24px;
  border-bottom: 2px solid black;
  white-space: nowrap;
  padding-left: 10px;
  padding-right: 10px;
}

.dropdown-item {
  color: rgb(136, 136, 136);
  cursor: pointer;
  font-family: 'Raleway', sans-serif;
  font-size: 24px;
  border-bottom: 2px solid black;
  white-space: nowrap;
  padding-left: 10px;
  padding-right: 10px;
}

.dropdown-item:hover {
  border-bottom: 2px solid lightseagreen;
  color: white !important;
  background-color: black;
}

.dropdown-divider {
  color: white;
}

.nav-item:hover {
  border-bottom: 2px solid lightseagreen;
  color: white !important;
}

a:hover {
  color: white !important;
}

.main-body {
  margin-left: 20%;
  margin-right: 20%;
  padding-top: 20px;
  font-size: 20px;
}

.panel-body {
  background-color: rgb(24, 24, 24);
  border: 2px solid rgb(123, 196, 192);
  border-radius: 10px;
  padding: 40px;
}

td {
  color: rgb(123, 196, 192);
  padding-top: 2px;
  padding-bottom: 2px;
  padding-left: 25px;
  padding-right: 25px;
}

p {
  color: rgb(200, 200, 200);
}

td:last-child {
  border-left: 1px solid grey;
}

.footer-text {
  text-align: center;
  font-family: "Inconsolata", monospace;
  color: white;
}

h1 {
  text-align: center;
  font-size: 64px;
  font-weight: normal;
  font-family: 'Raleway', sans-serif;
  padding-bottom: 20px;
  white-space: nowrap;
}

a {
  color: inherit;
  text-decoration: inherit;
}

hr {
  border: 1px solid white;
  margin-top:20px;
}

</style>
