<template>
  <main>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTogglerDemo03" aria-controls="navbarTogglerDemo03" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <a class="navbar-brand" style="color: #000000;" href="#">TIARA STYLE</a>

  <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
    <ul class="navbar-nav mr-auto">
                                <li class="nav-item active">
                                    <NuxtLink to="/" class="text-dark cd-md-3">
                                        Home
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/product" class="text-dark col-md-3">
                                        Product
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/contact" class="text-dark col-md-3">
                                        Contact
                                    </NuxtLink>
                                </li>
                            </ul>
  </div>
    </nav>
  </main>
</template>