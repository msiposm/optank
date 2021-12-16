<template>
  <div class="main">

    <!------------- NAVBAR/HEADER MENU ------------->
    <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-dark navbar-custom">
      <div class="container-fluid">
        <a class="navbar-brand" v-on:click="section = 'main'">Commonwealth of AWSome | Notification System</a>
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
                Actions
              </a>
              <ul class="dropdown-menu" aria-labelledby="navbarDropdown" style="background-color:black">
                <li><a class="dropdown-item" v-on:click="section = 'subscribe'">Subscribe</a></li>
                <li><a class="dropdown-item" v-on:click="section = 'create_feed'">Create Feed</a></li>
                <!--<li><hr class="dropdown-divider"></li>-->
                <li><a class="dropdown-item" v-on:click="section = 'notification'">Send Notification</a></li>
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

          <p class="project-item"></p>
          <p>- Example text</p>
        </div>
      </div>

      <!------------- SUBSCRIBE PAGE ------------->
      <div v-if="section == 'subscribe'" class="page-section">
        <h1>Subscribe to Notifications</h1>
        <div class="panel-body">
          <p style="font-weight: bold;">To subscribe to a notification, please complete the following form: </p>
          <form v-on:submit.prevent="subscribeForm">
            <div class='formField'>
              <p>Select a feed:</p>
              <!-- <select name="feed" v-model="subscribe.feed">
                <option value="feed_a">Feed A</option>
                <option value="feed_b">Feed B</option>
                <option value="feed_c">Feed C</option>
              </select> -->
            </div>
            <div class='formField'>
              <p>Enter your email address:</p>
              <input type="text" v-model="subscribe.email" placeholder="example@address.com" />
            </div>
            <div class='formField'>
              <input type="submit" value="Submit" />
            </div>
          </form>
        </div>
      </div>

      <!------------- "CREATE FEED" PAGE ------------->
      <div v-if="section == 'create_feed'" class="page-section">
        <h1>Create a New Feed</h1>
        <div class="panel-body">
          <p class="project-header" style="font-weight: bold;">To create a new feed, enter a title below and click 'Create'</p>
          <div>
            <form v-on:submit.prevent="feedForm">
              <div class='formField'>
              <input type="text" v-model="feed.email" placeholder="Title of Feed" />
              </div>
              <div class='formField'>
                <input type="submit" value="Create" />
                </div>
            </form>
          </div>
        </div>
      </div>

      <!----------- SUBMIT STORY PAGE ------------>
      <div v-if="section == 'notification'" class="page-section">
        <h1>Submit a Story to a Feed</h1>
        <div class="panel-body">
          <p>To submit a story to notification feed, please select a feed, enter the story details, and click "Submit"</p>
          <form v-on:submit.prevent="storyForm">
            <div class='formField'>
            <select name="feed" v-model="story.feed">
              <option value="feed_a">Feed A</option>
              <option value="feed_b">Feed B</option>
              <option value="feed_c">Feed C</option>
            </select>
            </div>
            <div class='formField'>
              <textarea v-model="story.description" placeholder="Notification details: " />
            </div>
            <div class='formField'>
            <input type="submit" value="Send" />
            </div>
          </form>
        </div>
      </div>

      <!----------- FOOTER -------------->
      <hr />
      <p class = "footer-text">Copyright &#169; 2021 Commonwealth of AWSome. All Rights Reserved</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'HelloWorld',
  data () {
    return {
      subscribe: {
        email: ''
        // feed: ''
      },
      feed: {
        email: ''
      },
      story: {
        description: '',
        feed: ''
      },
      section: 'main'
    }
  },

  methods: {
    async subscribeForm () {
      axios.put('https://iz7o3yh3p8.execute-api.ca-central-1.amazonaws.com/dev/subscribe', this.subscribe,
        {
          headers: {
            'content-type': 'application/json',
            'authorizationToken': 'YNQXmb4oYv9rSboLGFVmC5b9zszBfZtg5wcFVoD2',
            'Access-Control-Allow-Origin': '*'
          }
        }).then(response => { console.log(response) })
    },

    async feedForm () {
      axios.post('https://iz7o3yh3p8.execute-api.ca-central-1.amazonaws.com/dev/subscribe', this.feed,
        {
          headers: {
            'content-type': 'application/json',
            'authorizationToken': 'YNQXmb4oYv9rSboLGFVmC5b9zszBfZtg5wcFVoD2',
            'Access-Control-Allow-Origin': '*'
          }
        }
      )
    },

    async storyForm () {
      axios.post('https://iz7o3yh3p8.execute-api.ca-central-1.amazonaws.com/dev/subscribe', this.story,
        {
          headers: {
            'content-type': 'application/json',
            'authorizationToken': 'YNQXmb4oYv9rSboLGFVmC5b9zszBfZtg5wcFVoD2',
            'Access-Control-Allow-Origin': '*'
          }
        }
      )
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.formField {
  padding: 10px;
}

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
