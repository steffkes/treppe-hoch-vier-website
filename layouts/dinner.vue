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
            <div class="navbar-burger" data-target="navbar">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>

          <div id="navbar" class="navbar-menu">
            <div class="navbar-start">
              <a class="navbar-item is-tab is-active" href="/benefiz-gala">
                Benefiz-Gala
              </a>
              <a class="navbar-item is-tab" href="/"> Benefiz-Lauf </a>
            </div>
          </div>
        </nav>
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
        </div>
      </div>
    </section>
  </div>
</template>

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
