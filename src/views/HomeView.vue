<template>
  <div class="welcomeImage">

    <div class="topBar">

      <div class="iconBar">
          <div class="iconbarIcon">
            <i class="fab fa-twitter"></i>
            <i class="fab fa-facebook"></i>
            <i class="fab fa-linkedin"></i>
            <i class="fab fa-instagram"></i>
          </div>

          <h3>Open Hours of City Government Mon - Fri: 8:00am - 6:00pm</h3>

          <div class="searchIcon">
            <i class="far fa-search"></i>
          </div>
      </div>

      <div class="linkBar">

        <div class="logoContainer">
            <h1>IKLGA.</h1>
        </div>

        <div class="links">

          <div class="dropdown">
            <button class="dropbtn">Home</button>
            <div class="dropdown-content">
              <a href="#">Link 1</a>
              <a href="#">Link 2</a>
              <a href="#">Link 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Event</button>
            <div class="dropdown-content">
              <a href="#">Link 1</a>
              <a href="#">Link 2</a>
              <a href="#">Link 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Blog</button>
            <div class="dropdown-content">
              <a href="#">Link 1</a>
              <a href="#">Link 2</a>
              <a href="#">Link 3</a>
            </div>
          </div>

          <div class="dropdown">
            <button class="dropbtn">Landmark</button>
            <div class="dropdown-content">
              <a href="#">Link 1</a>
              <a href="#">Link 2</a>
              <a href="#">Link 3</a>
            </div>
          </div>

         <button class="contactus">Contact Us</button>
          
        </div>


      </div>

      

    </div>


    <div class="topBar2">

        <div id="main-content" class="main-content">
          <button @click="openSidebar()">Open Sidebar</button>
        </div>

        <div class="logoContainer" style="background-color: transparent;">
              <h1>IKLGA.</h1>
        </div>

        <div style="color:white">search</div>
    </div>

    <div class="sidebar" id="sidebar">

      <div class="sidebarlinks">

      </div>

      <div @click="closeSideBar()">X</div>


    </div>
    
  </div>
</template>

<script setup>

    function openSidebar(){
      const side = document.getElementById('sidebar')
      // side.style.display = 'block'
      side.style.marginLeft = '100%'
    }

    function closeSideBar(){
      const side = document.getElementById('sidebar')
      side.style.marginLeft = '-100%'
    }

</script>

<style scoped>

.welcomeImage{
  min-height: 110vh;
  width: 100%;
  background-image: url('../assets/images/louvre.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-color: rgb(167, 165, 165);
  background-blend-mode: multiply;
}

.topBar{
  height: auto;
  width: 75%;
  background-color: white;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
}

.iconBar{
  height: 3.5rem;
  width: 100%;
  background-color: rgba(218, 218, 218, 0.418);
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 0rem 1rem;
  color: gray;
  /* width: 20%; */
}

.iconbarIcon{
  width: 10%;
  display: flex;
  justify-content: space-evenly;
}
.linkBar{
  display: flex;
  flex-direction: row;
  height: 6rem;
  align-items: center;
}

.logoContainer{
  background-color: black;
  color: green;
  padding: 1.5rem 1.5rem;
  display: flex;
  align-items: center;
}


.links{
  height: 6rem;
  text-align: center;
  display: flex;
  width: 80%;
  justify-content: space-evenly;
}

.dropbtn {
  color: black;
  background-color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  height: 6rem;
  width: 6rem;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {background-color: #ddd;}

.dropdown:hover .dropdown-content {display: block;}

.dropdown:hover .dropbtn {color: #3e8e41;}

.contactus{
  height: 3rem; 
  align-self:center; 
  background-color: green; 
  color: white; 
  border: none; 
  border-radius: 30px;
  cursor: pointer;
  width: 8rem;
}

.topBar2{
  display: none;
}

@media (max-width: 910px) {

.topBar{
  display: none;
}

.topBar2{
  display: flex;
  height: 6rem;
  width: 100%;
  background-color: #353232;
  justify-content: space-evenly;
  align-items: center;
  z-index: 0.5;
}

  .sidebar{
    height: auto;
    width: 100%;
    /* overflow-y: auto; */
    border: 2px solid red;
    position: fixed;
    /* margin-left: -100%; */
    /* z-index: 1; */
    background-color: gray;    
    opacity: 0.6;
    visibility: visible;
    display: flex;
    flex-direction: row;
  }

  body.sidebar-active {
    overflow: hidden;
  }

  .sidebarlinks{
    min-height: 100vh;
    width: 90%;
    border: 2px solid yellow;
    /* z-index: 2; */

  }

  .welcomeImage{
    min-width: 100vh;
  }


}


</style>
