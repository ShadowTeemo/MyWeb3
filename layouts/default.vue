<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">about</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<slot />

<footer >
    <nav data-bs-theme="dark">
    <div class="card text-center">
  <div class="card-header">
    Footer
  </div>
  <div class="card-body">
    <h5 class="card-title">Thai Austrian Technical College</h5>
    <p class="card-text">66309010014</p>
    <p class="card-text">Mr.Ratchanon Pakdee</p>
  </div>
  <div class="card-footer text-body-secondary">
    FOOTER
  </div>
</div>
</nav>
</footer>

</template>

<style>
    body{margin: 0;padding: 0;}



</style>
