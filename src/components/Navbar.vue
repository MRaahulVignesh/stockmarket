<template>
    <nav class="navbar">
        <!-- LOGO -->
        <div class="logo">Crypto Market</div>
        <!-- NAVIGATION MENU -->
            <ul class="nav-links">
                <!-- USING CHECKBOX HACK -->
                <input type="checkbox" id="checkbox_toggle" />
                <label for="checkbox_toggle" class="hamburger">&#9776;</label>
                <!-- NAVIGATION MENUS -->
 <div class="menu">
 <li><a href="/">Home</a></li>
 <li><a href="/">Market Trends</a></li>
 <li><a href="/">Add Crypto</a></li>
 </div>
 </ul>
 </nav>
</template>

<style scoped>
.navbar {
 display: flex;
 align-items: center;
 justify-content: space-between;
 background-color: #F8AE1B;
 color: black
}
.nav-links a {
 color: black;
}
/* LOGO */
.logo {
    padding-left: 1rem;
    font-size: 24px;
    font-weight: bold;
}
/* NAVBAR MENU */
.menu {
 display: flex;
 gap: 1em;
 font-size: 18px;
 padding-right: 1rem;
 align-items: center;
}
.menu li:hover {
 background-color: #F8AE1B;
 border-radius: 5px;
 transition: 0.3s ease;
}
.menu li {
 padding: 5px 14px;
}
/* DROPDOWN MENU */
.services {
 position: relative; 
}
.dropdown {
 background-color: #F8AE1B;
 padding: 1em 0;
 position: absolute; /*WITH RESPECT TO PARENT*/
 display: none;
 border-radius: 8px;
 top: 35px;
}
.dropdown li + li {
 margin-top: 10px;
}
.dropdown li {
 padding: 0.5em 1em;
 width: 8em;
 text-align: center;
}
.dropdown li:hover {
 background-color: #F8AE1B;
}
.services:hover .dropdown {
 display: block;
}

input[type=checkbox]{
 display: none;
} 
/*HAMBURGER MENU*/
.hamburger {
 display: none;
 font-size: 24px;
 user-select: none;
 padding-right: 1rem;
}
/* APPLYING MEDIA QUERIES */
@media (max-width: 768px) {
.menu { 
 display:none;
 position: absolute;
 background-color:#F8AE1B;
 right: 0;
 left: 0;
 text-align: center;
 padding: 16px 0;
}
.menu li:hover {
 display: inline-block;
 background-color:#F8AE1B;
 transition: 0.3s ease;
}
.menu li + li {
 margin-top: 12px;
}
input[type=checkbox]:checked ~ .menu{
 display: block;
}
.hamburger {
 display: block;
}
.dropdown {
 left: 50%;
 top: 30px;
 transform: translateX(35%);
}
.dropdown li:hover {
 background-color: #F8AE1B;
}
}
</style>