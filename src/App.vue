<template>
  <div id="app">
    <!-- Navbar -->
    <nav class="navbar navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Navbar</a>
      </div>
    </nav>

    <!-- Links -->
    <ul class="container nav justify-content-center mt-4">
      <li class="nav-item"><router-link to="/">Home</router-link> | </li>
      <li class="nav-item ml-2">
        <router-link to="/about">&nbsp;About</router-link>
      </li>
      <li class="nav-item"></li>
      <li class="nav-item"></li>
    </ul>

    <router-view />
  </div>
</template>

<style></style>
