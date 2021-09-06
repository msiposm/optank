<template>
  <div class="hello">
    <div class = "header-menu">
      <div class = "header-item header-item-center" v-on:click="section = 'main'">
        ~/michael_sipos
      </div>
      <div class = "header-item header-item-text" v-on:click="section = 'about-me'">
        About Me
      </div>
      <div class = "header-item header-item-text" v-on:click="section = 'experience'">
        Experience
      </div>
      <div class = "header-item header-item-text" v-on:click="section = 'projects'">
        Projects
      </div>
      <div class = "header-item header-item-text" v-on:click="section = 'contact'">
        Contact
      </div>
    </div>
    <div class="main-body">
      <div v-if="section == 'main' || section == 'about-me'" class="page-section">
        <h1>About Me</h1>
        <div class="panel-body">
          <p>My name is Michael </p>
        </div>
      </div>

      <div v-if="section == 'experience'" class="page-section">
        <h1>Experience</h1>
        <div class="panel-body">
          <p>
            Hello There! Welcome to my website. Please feel free to click on the links above
         </p>
        </div>
      </div>

      <div v-if="section == 'projects'" class="page-section">
        <h1>Projects</h1>
        <div class="panel-body">
            <p>
              Hello There! Welcome to my website. Please feel free to click on the links above
          </p>
        </div>
      </div>

      <div v-if="section == 'contact'" class="page-section">
        <h1>Contact</h1>
        <div class="panel-body">
            <p>
              Hello There! Welcome to my website. Please feel free to click on the links above
          </p>
        </div>
      </div>

      <hr />
      <p class = "footer-text">
        &#169; Michael Sipos
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

@media (max-width: 768px) {
  .header-menu {
    flex-direction: column;
  }
}

.navbar {
  font-family: "Open Sans", sans-serif;
}

.header-item {
  flex: 1;
  text-align: center;
}

.header-item-center {
  text-align: left;
  font-family: 'Inconsolata', monospace;
  color: white;
  font-size: 32px;
}

.header-item-text {
  position: relative;
  color: rgb(136, 136, 136);
  font-size: 24px;
  cursor: pointer;
  padding: 20px;
  border-bottom: 2px solid black;
  width: fit-content;
  white-space: nowrap;
}

.header-item-text:hover {
  border-bottom: 2px solid lightseagreen;
  color: white;
}

.main-body {
  margin-left: 10%;
  margin-right: 10%;
}

.panel-body {
  background-color: rgb(36, 36, 36);
  border: 1px solid lightseagreen;
  border-radius: 5px;
  padding: 20px;
}

.footer-text {
  text-align: center;
  font-family: "Inconsolata", monospace;
}

h1 {
  font-size: 24px;
  font-weight: normal;
}

a {
  color: inherit;
  text-decoration: inherit;
}
</style>
