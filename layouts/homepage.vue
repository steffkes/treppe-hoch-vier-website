<template>
  <div style="background-color: #f9f9f9; min-height: 100vh">
    <section class="section">
      <div class="container is-max-desktop">
        <nav
          class="navbar is-transparent"
          style="background-color: transparent"
        >
          <div class="navbar-brand">
            <a class="navbar-item" href="/">
              <img src="/treppe-hoch-vier.svg" alt="TREPPE HOCH 4" />
            </a>
            <a
              role="button"
              class="navbar-burger"
              :class="{ 'is-active': activeNavbar }"
              aria-label="menu"
              aria-expanded="false"
              @click="activeNavbar = !activeNavbar"
            >
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
            </a>
          </div>

          <div class="navbar-menu" :class="{ 'is-active': activeNavbar }">
            <div class="navbar-start">
              <a class="navbar-item is-tab" href="/benefiz-lauf"
                >Benefiz-Lauf</a
              >
              <a class="navbar-item is-tab" href="/benefiz-gala">
                Benefiz-Gala
              </a>
            </div>
          </div>
        </nav>
      </div>
    </section>

    <section class="section pt-0">
      <div class="container">
        <div class="notification is-danger has-text-centered">
          Die Veranstaltung findet <strong>nicht</strong> statt.
        </div>
      </div>
    </section>

    <slot />

    <section class="section pb-0">
      <div class="container is-max-desktop">
        <h2 class="title is-3">Unsere Partner</h2>

        <div class="columns is-multiline is-vcentered grid">
          <div class="column is-4 has-text-centered">
            <a href="https://www.maritim.de/de/hotels/deutschland/hotel-ulm">
              <img src="/partner/maritim.svg"
            /></a>
          </div>
          <div class="column is-4 has-text-centered">
            <a href="https://www.donau3fm.de">
              <img src="/partner/donau3fm.svg" />
            </a>
          </div>
          <div class="column is-4 has-text-centered">
            <a href="https://www.kappelmeier-fotografie.de/">
              <img src="/partner/kappelmeier.png" />
            </a>
          </div>
          <div class="column is-4 has-text-centered">
            <a href="https://www.dietenbronner.de">
              <img src="/partner/dietenbronner.svg" />
            </a>
          </div>
          <div class="column is-4 has-text-centered">
            <a href="https://www.seeberger.de">
              <img src="/partner/seeberger.svg" />
            </a>
          </div>
          <div class="column is-4 has-text-centered">
            <a href="https://www.uniklinik-ulm.de/">
              <img src="/partner/uniklinik-ulm.svg" />
            </a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const activeNavbar = ref(false);
</script>

<style>
.grid img {
  /*aspect-ratio: 3/2;*/
  filter: grayscale(1);
}
.grid img.invert {
  filter: invert(1);
}
.grid img.reduced {
  opacity: 0.7;
}
</style>
