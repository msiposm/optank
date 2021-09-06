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
                <li><a class="dropdown-item" v-on:click="section = 'projects'">Project 1</a></li>
                <li><a class="dropdown-item" v-on:click="section = 'projects'">Project 2</a></li>
                <li><hr class="dropdown-divider"></li>
                <li><a class="dropdown-item" v-on:click="section = 'projects'">Project 3</a></li>
              </ul>
            </li>
            <li class="nav-item header-item-text">
              <a class="nav-link" v-on:click="section = 'contact'">Contact</a>
            </li>
            <li class="nav-item">
              <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Projects <i>(coming soon)</i></a>
            </li>
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
          <p>Sem fringilla ut morbi tincidunt augue interdum velit euismod. Tempor id eu nisl nunc mi ipsum faucibus. Nunc vel risus commodo viverra maecenas accumsan lacus vel facilisis. Et tortor at risus viverra. Proin sagittis nisl rhoncus mattis rhoncus urna neque. Congue quisque egestas diam in arcu. At risus viverra adipiscing at in tellus integer feugiat. Turpis egestas pretium aenean pharetra magna ac placerat vestibulum lectus. Donec massa sapien faucibus et molestie ac feugiat sed lectus. Congue mauris rhoncus aenean vel elit scelerisque mauris. Id cursus metus aliquam eleifend mi in nulla posuere. In hac habitasse platea dictumst vestibulum rhoncus est pellentesque elit. Enim tortor at auctor urna nunc id cursus metus aliquam. A cras semper auctor neque vitae tempus quam pellentesque nec. Elit ut aliquam purus sit. Tortor condimentum lacinia quis vel eros donec ac odio tempor.</p>
          <p>Sed tempus urna et pharetra. Lacus viverra vitae congue eu consequat ac felis donec et. Ullamcorper malesuada proin libero nunc consequat interdum varius sit. Eget mauris pharetra et ultrices. Maecenas ultricies mi eget mauris pharetra et ultrices. Porta non pulvinar neque laoreet suspendisse interdum consectetur. Eget sit amet tellus cras adipiscing. Facilisis gravida neque convallis a cras semper auctor. Ut sem viverra aliquet eget. Pellentesque dignissim enim sit amet venenatis urna cursus eget nunc. Id nibh tortor id aliquet lectus. Porttitor leo a diam sollicitudin tempor id. Nullam eget felis eget nunc lobortis mattis aliquam faucibus.</p>
          <p>Nec dui nunc mattis enim ut tellus elementum sagittis vitae. Rutrum quisque non tellus orci ac auctor. Mauris pharetra et ultrices neque ornare. Quam vulputate dignissim suspendisse in est ante in nibh mauris. Elementum pulvinar etiam non quam lacus suspendisse faucibus interdum. Pellentesque nec nam aliquam sem et tortor. Vel fringilla est ullamcorper eget. Consequat id porta nibh venenatis cras sed felis eget. Neque egestas congue quisque egestas diam in arcu. Arcu cursus euismod quis viverra nibh cras pulvinar. Pretium nibh ipsum consequat nisl vel pretium lectus quam. Aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices.</p>
          <p>Et leo duis ut diam quam nulla porttitor. Turpis egestas sed tempus urna et pharetra pharetra massa. Elit duis tristique sollicitudin nibh. Eu mi bibendum neque egestas congue quisque egestas diam. Adipiscing bibendum est ultricies integer quis auctor elit sed vulputate. Duis convallis convallis tellus id interdum velit laoreet id donec. Purus in massa tempor nec feugiat nisl. Eu lobortis elementum nibh tellus molestie nunc. Fames ac turpis egestas maecenas. Faucibus ornare suspendisse sed nisi lacus sed viverra tellus. Pulvinar pellentesque habitant morbi tristique senectus et netus et. Varius quam quisque id diam vel quam elementum. Consectetur lorem donec massa sapien faucibus et molestie. Tincidunt augue interdum velit euismod in. Aliquet nibh praesent tristique magna sit amet. Feugiat pretium nibh ipsum consequat nisl. Mattis ullamcorper velit sed ullamcorper morbi tincidunt. Metus aliquam eleifend mi in nulla. Et netus et malesuada fames.</p>
        </div>
      </div>

      <div v-if="section == 'experience'" class="page-section">
        <h1>Experience</h1>
        <div class="panel-body">
          <p>Hello There! Welcome to my website. Please feel free to click on the links above</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Gravida rutrum quisque non tellus orci ac auctor. Enim diam vulputate ut pharetra sit amet aliquam id. Volutpat lacus laoreet non curabitur gravida arcu ac tortor dignissim. Convallis posuere morbi leo urna molestie at elementum eu. Amet purus gravida quis blandit turpis cursus in hac. Pellentesque elit eget gravida cum sociis natoque. Nunc aliquet bibendum enim facilisis gravida neque convallis a cras. Est sit amet facilisis magna etiam tempor orci. Nunc consequat interdum varius sit amet mattis. Mi sit amet mauris commodo quis imperdiet massa tincidunt nunc. Sit amet est placerat in egestas erat imperdiet sed. Pretium nibh ipsum consequat nisl vel pretium. Ac turpis egestas sed tempus urna et pharetra pharetra. Consequat mauris nunc congue nisi vitae.</p>
          <p>Sem fringilla ut morbi tincidunt augue interdum velit euismod. Tempor id eu nisl nunc mi ipsum faucibus. Nunc vel risus commodo viverra maecenas accumsan lacus vel facilisis. Et tortor at risus viverra. Proin sagittis nisl rhoncus mattis rhoncus urna neque. Congue quisque egestas diam in arcu. At risus viverra adipiscing at in tellus integer feugiat. Turpis egestas pretium aenean pharetra magna ac placerat vestibulum lectus. Donec massa sapien faucibus et molestie ac feugiat sed lectus. Congue mauris rhoncus aenean vel elit scelerisque mauris. Id cursus metus aliquam eleifend mi in nulla posuere. In hac habitasse platea dictumst vestibulum rhoncus est pellentesque elit. Enim tortor at auctor urna nunc id cursus metus aliquam. A cras semper auctor neque vitae tempus quam pellentesque nec. Elit ut aliquam purus sit. Tortor condimentum lacinia quis vel eros donec ac odio tempor.</p>
          <p>Sed tempus urna et pharetra. Lacus viverra vitae congue eu consequat ac felis donec et. Ullamcorper malesuada proin libero nunc consequat interdum varius sit. Eget mauris pharetra et ultrices. Maecenas ultricies mi eget mauris pharetra et ultrices. Porta non pulvinar neque laoreet suspendisse interdum consectetur. Eget sit amet tellus cras adipiscing. Facilisis gravida neque convallis a cras semper auctor. Ut sem viverra aliquet eget. Pellentesque dignissim enim sit amet venenatis urna cursus eget nunc. Id nibh tortor id aliquet lectus. Porttitor leo a diam sollicitudin tempor id. Nullam eget felis eget nunc lobortis mattis aliquam faucibus.</p>
          <p>Nec dui nunc mattis enim ut tellus elementum sagittis vitae. Rutrum quisque non tellus orci ac auctor. Mauris pharetra et ultrices neque ornare. Quam vulputate dignissim suspendisse in est ante in nibh mauris. Elementum pulvinar etiam non quam lacus suspendisse faucibus interdum. Pellentesque nec nam aliquam sem et tortor. Vel fringilla est ullamcorper eget. Consequat id porta nibh venenatis cras sed felis eget. Neque egestas congue quisque egestas diam in arcu. Arcu cursus euismod quis viverra nibh cras pulvinar. Pretium nibh ipsum consequat nisl vel pretium lectus quam. Aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices.</p>
          <p>Et leo duis ut diam quam nulla porttitor. Turpis egestas sed tempus urna et pharetra pharetra massa. Elit duis tristique sollicitudin nibh. Eu mi bibendum neque egestas congue quisque egestas diam. Adipiscing bibendum est ultricies integer quis auctor elit sed vulputate. Duis convallis convallis tellus id interdum velit laoreet id donec. Purus in massa tempor nec feugiat nisl. Eu lobortis elementum nibh tellus molestie nunc. Fames ac turpis egestas maecenas. Faucibus ornare suspendisse sed nisi lacus sed viverra tellus. Pulvinar pellentesque habitant morbi tristique senectus et netus et. Varius quam quisque id diam vel quam elementum. Consectetur lorem donec massa sapien faucibus et molestie. Tincidunt augue interdum velit euismod in. Aliquet nibh praesent tristique magna sit amet. Feugiat pretium nibh ipsum consequat nisl. Mattis ullamcorper velit sed ullamcorper morbi tincidunt. Metus aliquam eleifend mi in nulla. Et netus et malesuada fames.</p>

        </div>
      </div>

      <div v-if="section == 'projects'" class="page-section">
        <h1>Projects</h1>
        <div class="panel-body">
          <p>Hello There! Welcome to my website. Please feel free to click on the links above</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Gravida rutrum quisque non tellus orci ac auctor. Enim diam vulputate ut pharetra sit amet aliquam id. Volutpat lacus laoreet non curabitur gravida arcu ac tortor dignissim. Convallis posuere morbi leo urna molestie at elementum eu. Amet purus gravida quis blandit turpis cursus in hac. Pellentesque elit eget gravida cum sociis natoque. Nunc aliquet bibendum enim facilisis gravida neque convallis a cras. Est sit amet facilisis magna etiam tempor orci. Nunc consequat interdum varius sit amet mattis. Mi sit amet mauris commodo quis imperdiet massa tincidunt nunc. Sit amet est placerat in egestas erat imperdiet sed. Pretium nibh ipsum consequat nisl vel pretium. Ac turpis egestas sed tempus urna et pharetra pharetra. Consequat mauris nunc congue nisi vitae.</p>
          <p>Sem fringilla ut morbi tincidunt augue interdum velit euismod. Tempor id eu nisl nunc mi ipsum faucibus. Nunc vel risus commodo viverra maecenas accumsan lacus vel facilisis. Et tortor at risus viverra. Proin sagittis nisl rhoncus mattis rhoncus urna neque. Congue quisque egestas diam in arcu. At risus viverra adipiscing at in tellus integer feugiat. Turpis egestas pretium aenean pharetra magna ac placerat vestibulum lectus. Donec massa sapien faucibus et molestie ac feugiat sed lectus. Congue mauris rhoncus aenean vel elit scelerisque mauris. Id cursus metus aliquam eleifend mi in nulla posuere. In hac habitasse platea dictumst vestibulum rhoncus est pellentesque elit. Enim tortor at auctor urna nunc id cursus metus aliquam. A cras semper auctor neque vitae tempus quam pellentesque nec. Elit ut aliquam purus sit. Tortor condimentum lacinia quis vel eros donec ac odio tempor.</p>
          <p>Sed tempus urna et pharetra. Lacus viverra vitae congue eu consequat ac felis donec et. Ullamcorper malesuada proin libero nunc consequat interdum varius sit. Eget mauris pharetra et ultrices. Maecenas ultricies mi eget mauris pharetra et ultrices. Porta non pulvinar neque laoreet suspendisse interdum consectetur. Eget sit amet tellus cras adipiscing. Facilisis gravida neque convallis a cras semper auctor. Ut sem viverra aliquet eget. Pellentesque dignissim enim sit amet venenatis urna cursus eget nunc. Id nibh tortor id aliquet lectus. Porttitor leo a diam sollicitudin tempor id. Nullam eget felis eget nunc lobortis mattis aliquam faucibus.</p>
          <p>Nec dui nunc mattis enim ut tellus elementum sagittis vitae. Rutrum quisque non tellus orci ac auctor. Mauris pharetra et ultrices neque ornare. Quam vulputate dignissim suspendisse in est ante in nibh mauris. Elementum pulvinar etiam non quam lacus suspendisse faucibus interdum. Pellentesque nec nam aliquam sem et tortor. Vel fringilla est ullamcorper eget. Consequat id porta nibh venenatis cras sed felis eget. Neque egestas congue quisque egestas diam in arcu. Arcu cursus euismod quis viverra nibh cras pulvinar. Pretium nibh ipsum consequat nisl vel pretium lectus quam. Aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices.</p>
          <p>Et leo duis ut diam quam nulla porttitor. Turpis egestas sed tempus urna et pharetra pharetra massa. Elit duis tristique sollicitudin nibh. Eu mi bibendum neque egestas congue quisque egestas diam. Adipiscing bibendum est ultricies integer quis auctor elit sed vulputate. Duis convallis convallis tellus id interdum velit laoreet id donec. Purus in massa tempor nec feugiat nisl. Eu lobortis elementum nibh tellus molestie nunc. Fames ac turpis egestas maecenas. Faucibus ornare suspendisse sed nisi lacus sed viverra tellus. Pulvinar pellentesque habitant morbi tristique senectus et netus et. Varius quam quisque id diam vel quam elementum. Consectetur lorem donec massa sapien faucibus et molestie. Tincidunt augue interdum velit euismod in. Aliquet nibh praesent tristique magna sit amet. Feugiat pretium nibh ipsum consequat nisl. Mattis ullamcorper velit sed ullamcorper morbi tincidunt. Metus aliquam eleifend mi in nulla. Et netus et malesuada fames.</p>
        </div>
      </div>

      <div v-if="section == 'contact'" class="page-section">
        <h1>Contact</h1>
        <div class="panel-body">
          <p>Hello There! Welcome to my website. Please feel free to click on the links above</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Gravida rutrum quisque non tellus orci ac auctor. Enim diam vulputate ut pharetra sit amet aliquam id. Volutpat lacus laoreet non curabitur gravida arcu ac tortor dignissim. Convallis posuere morbi leo urna molestie at elementum eu. Amet purus gravida quis blandit turpis cursus in hac. Pellentesque elit eget gravida cum sociis natoque. Nunc aliquet bibendum enim facilisis gravida neque convallis a cras. Est sit amet facilisis magna etiam tempor orci. Nunc consequat interdum varius sit amet mattis. Mi sit amet mauris commodo quis imperdiet massa tincidunt nunc. Sit amet est placerat in egestas erat imperdiet sed. Pretium nibh ipsum consequat nisl vel pretium. Ac turpis egestas sed tempus urna et pharetra pharetra. Consequat mauris nunc congue nisi vitae.</p>
          <p>Sem fringilla ut morbi tincidunt augue interdum velit euismod. Tempor id eu nisl nunc mi ipsum faucibus. Nunc vel risus commodo viverra maecenas accumsan lacus vel facilisis. Et tortor at risus viverra. Proin sagittis nisl rhoncus mattis rhoncus urna neque. Congue quisque egestas diam in arcu. At risus viverra adipiscing at in tellus integer feugiat. Turpis egestas pretium aenean pharetra magna ac placerat vestibulum lectus. Donec massa sapien faucibus et molestie ac feugiat sed lectus. Congue mauris rhoncus aenean vel elit scelerisque mauris. Id cursus metus aliquam eleifend mi in nulla posuere. In hac habitasse platea dictumst vestibulum rhoncus est pellentesque elit. Enim tortor at auctor urna nunc id cursus metus aliquam. A cras semper auctor neque vitae tempus quam pellentesque nec. Elit ut aliquam purus sit. Tortor condimentum lacinia quis vel eros donec ac odio tempor.</p>
          <p>Sed tempus urna et pharetra. Lacus viverra vitae congue eu consequat ac felis donec et. Ullamcorper malesuada proin libero nunc consequat interdum varius sit. Eget mauris pharetra et ultrices. Maecenas ultricies mi eget mauris pharetra et ultrices. Porta non pulvinar neque laoreet suspendisse interdum consectetur. Eget sit amet tellus cras adipiscing. Facilisis gravida neque convallis a cras semper auctor. Ut sem viverra aliquet eget. Pellentesque dignissim enim sit amet venenatis urna cursus eget nunc. Id nibh tortor id aliquet lectus. Porttitor leo a diam sollicitudin tempor id. Nullam eget felis eget nunc lobortis mattis aliquam faucibus.</p>
          <p>Nec dui nunc mattis enim ut tellus elementum sagittis vitae. Rutrum quisque non tellus orci ac auctor. Mauris pharetra et ultrices neque ornare. Quam vulputate dignissim suspendisse in est ante in nibh mauris. Elementum pulvinar etiam non quam lacus suspendisse faucibus interdum. Pellentesque nec nam aliquam sem et tortor. Vel fringilla est ullamcorper eget. Consequat id porta nibh venenatis cras sed felis eget. Neque egestas congue quisque egestas diam in arcu. Arcu cursus euismod quis viverra nibh cras pulvinar. Pretium nibh ipsum consequat nisl vel pretium lectus quam. Aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices.</p>
          <p>Et leo duis ut diam quam nulla porttitor. Turpis egestas sed tempus urna et pharetra pharetra massa. Elit duis tristique sollicitudin nibh. Eu mi bibendum neque egestas congue quisque egestas diam. Adipiscing bibendum est ultricies integer quis auctor elit sed vulputate. Duis convallis convallis tellus id interdum velit laoreet id donec. Purus in massa tempor nec feugiat nisl. Eu lobortis elementum nibh tellus molestie nunc. Fames ac turpis egestas maecenas. Faucibus ornare suspendisse sed nisi lacus sed viverra tellus. Pulvinar pellentesque habitant morbi tristique senectus et netus et. Varius quam quisque id diam vel quam elementum. Consectetur lorem donec massa sapien faucibus et molestie. Tincidunt augue interdum velit euismod in. Aliquet nibh praesent tristique magna sit amet. Feugiat pretium nibh ipsum consequat nisl. Mattis ullamcorper velit sed ullamcorper morbi tincidunt. Metus aliquam eleifend mi in nulla. Et netus et malesuada fames.</p>
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

.navbar-custom {
  font-family: "Open Sans", sans-serif;
  background-color: black !important;
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
  font-family: "Open Sans", sans-serif;
  font-size: 24px;
  border-bottom: 2px solid black;
  white-space: nowrap;
  padding-left: 10px;
  padding-right: 10px;
}

.dropdown-item {
  color: rgb(136, 136, 136);
  cursor: pointer;
  font-family: "Open Sans", sans-serif;
  font-size: 18px;
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
}

.panel-body {
  background-color: rgb(36, 36, 36);
  border: 2px solid lightseagreen;
  border-radius: 10px;
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
