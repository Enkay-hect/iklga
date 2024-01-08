<template>

<div class="sidebar" id="sidebar" >

  <div class="sidebarlinks">

  </div>

  <div @click="closeSideBar()"><svg xmlns="http://www.w3.org/2000/svg" height="32" width="32" viewBox="0 0 384 512" style="fill: white; stroke: black; stroke-width: 2px; margin-top: 3rem;"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"/>--></svg></div>

</div>

  <div class="welcomeImage">

    <div class="topBar">

      <div class="iconBar">
          <div class="iconbarIcon">
            <i class="fab fa-twitter"></i>
            <i class="fab fa-facebook"></i>
            <i class="fab fa-linkedin"></i>
            <i class="fab fa-instagram"></i>
            <i class="fa-check"></i>
            <!-- <i class="fa-solid fa-check"></i>
            <i class="fa fa-user"></i> -->
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

          <div  @click="openSideBar()"><svg xmlns="http://www.w3.org/2000/svg" height="32" width="28" viewBox="0 0 448 512" style="fill: white; stroke: black; stroke-width: 2px;"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/>--></svg></div>

        <div class="logoContainer" style="background-color: transparent;">
              <h1>IKLGA.</h1>
        </div>

        <div style="color:white"><svg xmlns="http://www.w3.org/2000/svg" height="32" width="32" viewBox="0 0 512 512" style="fill: white; stroke: black; stroke-width: 2px;"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"/>--></svg></div>
    </div>
    
  </div>
</template>

<script setup>

    function openSideBar(){
      const openside = document.getElementById('sidebar')

       const computedStyle = window.getComputedStyle(openside);

        if(computedStyle.display == 'none'){
          openside.style.display = 'flex'
        }
    }

    function closeSideBar(){
      const closeside = document.getElementById('sidebar')
      closeside.style.display = 'none'
    }

</script>

<style scoped>

.welcomeImage{
  min-height: 100vh;
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

.sidebar{
  display: none;
}

@media (max-width: 910px) {

.topBar{
  display: none;
}

.topBar2{
  display: flex;
  flex-direction: row;
  height: 6rem;
  width: 100%;
  background-color: #353232;
  justify-content: space-evenly;
  align-items: center;
  z-index: 0;
  position: relative;
}

  .sidebar{
    height: auto;
    width: 100%;
    position: fixed;
    background-color: #353232;    
    /* opacity: 0.6; */
    visibility: visible;
    display: none;
    flex-direction: row;
    z-index: 1;
  }

  body.sidebar-active {
    overflow: hidden;
    background-color: #353232;    

  }

  .sidebarlinks{
    min-height: 200vh;
    width: 90%;
    /* z-index: 2; */

  }


}


</style>
