<template>
  <div class="main">

    <!------------- NAVBAR/HEADER MENU ------------->
    <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark navbar-custom">
      <div class="container-fluid">
        <a class="navbar-brand" v-on:click="section = 'main'">AWSome Government</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item header-item-text">
              <a class="nav-link" aria-current="page" v-on:click="section = 'main'">Home</a>
              <!-- <a class="nav-link active" aria-current="page" href="#">Home</a> -->
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                AWSome Government Notifications
              </a>
              <ul class="dropdown-menu" aria-labelledby="navbarDropdown" style="background-color:black">
                <li><a class="dropdown-item" v-on:click="section = 'subscribe'">Subscribe</a></li>
                <li><a class="dropdown-item" v-on:click="section = 'create_feed'">Create Feed</a></li>
                <!--<li><hr class="dropdown-divider"></li>-->
                <li><a class="dropdown-item" v-on:click="section = 'notification'">Submit Notification</a></li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!------------- HOME ------------->
    <div class="main-body">
      <div v-if="section == 'main' || section == 'about-me'" class="page-section">
        <h1>Home</h1>
        <div class="panel-body">
          <p style="color:white;">👋 Hello, there! Welcome to the Commonwealth of AWSome</p>
          <form v-on:submit.prevent="submitForm">
            <input type="text" v-model="email" placeholder="Enter email address: " />
            <input type="submit" value="Submit" />
            <!-- Input of any type and tectareas goes here -->
          </form>
          <p class="project-item"></p>
          <p>- Example text</p>
        </div>
      </div>

      <!------------- SUBSCRIBE PAGE ------------->
      <div v-if="section == 'subscribe'" class="page-section">
        <h1>Subscribe</h1>
        <div class="panel-body">
          <p style="font-weight: bold;">What you're looking at right now!</p>
          <p>To subscribe, please hit subscribe</p>
        </div>
      </div>

      <!------------- "CREATE FEED" PAGE ------------->
      <div v-if="section == 'create_feed'" class="page-section">
        <h1>Create a New Feed</h1>
        <div class="panel-body">
          <p class="project-header" style="font-weight: bold;">Project details coming soon!</p>
          <div>
            <p class="project-header">hgfdh</p>
          </div>
        </div>
      </div>

      <!----------- SUBMIT NOTIFICATION PAGE ------------>
      <div v-if="section == 'notification'" class="page-section">
        <h1>Projects</h1>
        <div class="panel-body">
          <p>This section is currently under development. Please visit again soon to see more projects!</p>
        </div>
      </div>

      <!----------- FOOTER -------------->
      <hr />
      <p class = "footer-text">Copyright &#169; 2021 Commonwealth of AWSome. All Rights Reserved</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      email: '',
      section: 'main'
    }
  },

  methods: {
    async submitForm () {
      const res = await fetch('https://iz7o3yh3p8.execute-api.ca-central-1.amazonaws.com/dev/subscribe', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json', 'Access-Control-Allow-Origin': '*' },
        body: JSON.stringify({email: this.email})
      })
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
  margin-left: 10%;
  margin-right: 10%;
  padding-top: 20px;
  font-size: 16px;
}

.panel-body {
  background-color: rgb(24, 24, 24);
  border: 2px solid rgb(123, 196, 192);
  border-radius: 10px;
  padding: 20px;
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
  font-size: 48px;
  font-weight: normal;
  font-family: 'Raleway', sans-serif;
  padding-bottom: 20px;
  white-space: nowrap;
}

.project-item {
  color: rgb(123, 196, 192);
  font-family: "Inconsolata", monospace;
  margin-left: 20px;
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
