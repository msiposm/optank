<template>
  <div class="main">

    <!------------- NAVBAR/HEADER MENU ------------->
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
                <li><a class="dropdown-item" v-on:click="section = 'linuxProjects'">Linux Projects</a></li>
                <!--<li><hr class="dropdown-divider"></li>-->
                <li><a class="dropdown-item" v-on:click="section = 'projects'">Projects</a></li>
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

    <!------------- MAIN/ABOUT ME PAGE ------------->
    <div class="main-body">
      <div v-if="section == 'main' || section == 'about-me'" class="page-section">
        <h1>About Me</h1>
        <div class="panel-body">
          <p style="color:white;">👋 Hello, there! I’m Michael Sipos</p>
          <p>- 👀 I’m interested in ...</p>
          <p class="project-item"> Linux, full-stack development, creating elegant and responsive software solutions, and <em>constantly</em> learning</p>
          <p>- 🌱 I’m currently learning ... </p>
          <p class="project-item"> Num.py and Sci.py for evaluation of engineering/applied mathematical problems and large-scale data analysis</p>
          <p>- 💞️ I’m looking to collaborate on ... </p>
          <p class="project-item">Minimalist open-source applications with a lean footprint</p>
          <p>- 🌲 Outside of tech, I like to ... </p>
          <p class="project-item">🎼 Listen to music (Bach is my #1)! I play guitar in a band, solo classical guitar, and try my hand(s) at piano and violin</p>
          <p class="project-item">❄️ Freeze! I like the cold, and enjoy the winters skiing, backpacking, XC skiing, and ice skating</p>
          <p class="project-item">☀️ When it gets warmer, I like biking, kayaking, and stargazing</p>
          <p class="project-item">📷 I'm a cinephile, avid reader, and photography enthusiast</p>
          <p>- 📫 How to reach me ... </p>
          <p class="project-item">
            <a href="#">
              <img src="../assets/github.png"> Github
            </a>
            <a href="https://www.linkedin.com/in/siposm">
              <img src="../assets/linkedin.png"> LinkedIn
            </a>
          </p>
        </div>
      </div>

      <!------------- EXPERIENCE PAGE ------------->
      <div v-if="section == 'experience'" class="page-section">
        <h1>Experience</h1>
        <div class="panel-body">
          <p>This section is currently under development. Please visit again soon!</p>
        </div>
      </div>

      <!------------- WEBSITE PAGE ------------->
      <div v-if="section == 'website'" class="page-section">
        <h1>Website</h1>
        <div class="panel-body">
          <p style="font-weight: bold;">What you're looking at right now!</p>
          <p>This website was custom-developed in HTML/CSS/JS using a MEVN full-stack web development framework.</p>
          <!------ TABLE 1 ------>
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
          <p>Hosting is provided through Amazon Web Services (AWS) using GitHub as code repository. A Build / Test / Deploy process is implemented through AWS cloud CI/CD tools. With a simple GitHub push, the pipeline is automatically triggered!</p>
          <p>Additional libraries and tools used:</p>
          <!------ TABLE 2 ------>
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

      <!------------- "LINUX PROJECTS" PAGE ------------->
      <div v-if="section == 'linuxProjects'" class="page-section">
        <h1>Linux Projects</h1>
        <div class="panel-body">
          <p class="project-header" style="font-weight: bold;">Project details coming soon!</p>
          <div>
            <p class="project-header">Project: Squid Proxy-Caching Server for Web Acceleration</p>
            <ul>
              <li class="project-item">Caching static content </li>
              <li class="project-item">Authentication</li>
              <li class="project-item">Logging and filtering</li>
              <li class="project-item">Reverse proxy and load balancing</li>
            </ul>
            <p class="project-header">Project: OpenSSH, Stunnel, SOCKS Proxies</p>
            <ul>
              <li class="project-item">Setting up OpenSSH and hardening the out-of-box configurations</li>
              <li class="project-item">Using OpenSSH for tunneling and configuring a SOCKS proxy</li>
              <li class="project-item">Using Stunnel for tunneling and securing TCP protocols</li>
              <li class="project-item">Remote desktop connection with VNC over encrypted channels</li>
            </ul>
            <p class="project-header">Project: Linux Firewall Configuration</p>
            <ul>
              <li class="project-item">Setting up a stateful firewall with linux kernel firewall iptables/netfilter</li>
              <li class="project-item">Block unwanted requests with fail2ban and the iptables 'limit' module</li>
              <li class="project-item">Setting up logging systems, sending encrypted emails from host with local mail server</li>
            </ul>
            <p class="project-header">Project: Creating a Custom BIND Server</p>
            <ul>
              <li class="project-item">Caching DNS server for personal network</li>
              <li class="project-item">Combining BIND with Squid for web acceleration</li>
            </ul>
            <p class="project-header">Project: OpenVPN from Scratch</p>
            <ul>
              <li class="project-item">Setting up a personal Virtual Private Network (VPN) using the open-source OpenVPN system</li>
              <li class="project-item">Using OpenVPN to securely host VPN-only services</li>
              <li class="project-item">Connecting Windows, Linux, iOS, and Android devices to openVPN</li>
            </ul>
            <p class="project-header">Project: Encryption/Cryptography and Public-Key Infrastructure (PKI)</p>
            <ul>
              <li class="project-item">Linux encryption with gnupg, openssl, p7zip</li>
              <li class="project-item">Self-signed S/MIME certificates for email signing/encryption</li>
              <li class="project-item">Linux disk/volume encryption: LUKS/dm-crypt/cryptsetup</li>
              <li class="project-item">FUSE, Virtual File Systems, chroot</li>
            </ul>
            <p class="project-header">Project: Linux Audio Systems and Hi-Fi Audio</p>
            <ul>
              <li class="project-item">ALSA, alsaconf, .asoundrc, PulseAudio configuration</li>
              <li class="project-item">Low-latency audio with JACK and real-time kernels</li>
              <li class="project-item">Music server with mpd, ncurses clients (ncmpc/ncmpcpp)</li>
              <li class="project-item">Lossless CD ripping and conversion (RubyRipper, freedb/gnudb validation)</li>
            </ul>
            <p class="project-header">Project: Backup, Data Transfer, Secure Erasure</p>
            <ul>
              <li class="project-item">Using Rsync for local and remote manual/automated backups</li>
              <li class="project-item">Using SFTP for encrypted file transfer</li>
              <li class="project-item">Linux-based secure FTP with hardened FTPS and FTPES</li>
              <li class="project-item">Barebones data transfer: learning to use 'dd'</li>
              <li class="project-item">Blowing it up with Darik's Boot and Nuke (DBAN), and other data copying/partitioning live environments</li>
            </ul>
            <p class="project-header">Project: Network Analysis and Cybersecurity</p>
            <ul>
              <li class="project-item">Packet sniffing with tcpdump, wireshark; wireless chips with monitor/promiscuous mode</li>
              <li class="project-item">Port scanning with nmap</li>
              <li class="project-item">Open-source Intrusion Prevention System with snort</li>
              <li class="project-item">Aircrack-ng wireless cracking suite (Aireplay,Airodump,Airbase)</li>
              <li class="project-item">Slowloris attacks with SlowHTTPTest and PyLoris</li>
              <li class="project-item">Penetration testing with BackTrack Linux (now Kali) and exploit suites (nikto, kismet, w3af, metasploit)</li>
              <li class="project-item">Importance of strong passwords, good hash algorithms, and testing Ophcrack to crack Windows/NT passwords</li>
              <li class="project-item">Secure live environment with Tails</li>
              <li class="project-item">Open-source malware scanning with ClamAV</li>
              <li class="project-item">Linux system monitoring tools: conky, vmstat, vnstat, iptraf, ntop, (h)top, lsof, ss, netstat, iftop, iotop, iostat</li>
            </ul>
            <p class="project-header">Linux OS Distribution Reviews</p>
            <ul>
              <li class="project-item">Building Linux from Scratch, with Linux From Scratch (LFS)</li>
              <li class="project-item">Arch Linux and derivatives, the Arch Linux philosophy</li>
              <li class="project-item">Gentoo</li>
              <li class="project-item">Slackware</li>
              <li class="project-item">Debian and derivatives</li>
              <li class="project-item">RHEL and family (Fedora, Scientific OS, CentOS)</li>
              <li class="project-item">OpenSUSE</li>
              <li class="project-item">*BSD Operating Systems</li>
              <li class="project-item">Specialty distributions, run-from-RAM, old PCs (DamnSmallLinux, Puppy, TinyCore, SliTaz)</li>
            </ul>
            <p class="project-header">Linux Desktop Environment and Window Manager Reviews</p>
            <ul>
              <li class="project-item">Gnome 2, Gnome 3</li>
              <li class="project-item">KDE</li>
              <li class="project-item">XFCE, LXDE, LXQt</li>
              <li class="project-item">Tiling Window Managers: awesome, dwm, i3, spectrwm, xmonad, ratpoison</li>
              <li class="project-item">Stacking Window Managers: openbox, fluxbox, icewm</li>
            </ul>
          </div>
        </div>
      </div>

      <!----------- PROJECTS PAGE ------------>
      <div v-if="section == 'projects'" class="page-section">
        <h1>Projects</h1>
        <div class="panel-body">
          <p>This section is currently under development. Please visit again soon to see more projects!</p>
        </div>
      </div>

      <!----------- FOOTER -------------->
      <hr />
      <p class = "footer-text">Copyright &#169; 2021 Michael Sipos. All Rights Reserved</p>
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
