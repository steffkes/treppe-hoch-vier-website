<template>
  <div style="background-color: #f9f9f9; min-height: 100vh">
    <section class="section pb-0">
      <div class="container is-max-desktop">
        <div class="columns">
          <div class="column is-8">
            <h1 class="title is-1 mb-6">
              <a href="/">
                <img src="/treppe-hoch-vier.svg" alt="TREPPE HOCH 4" />
              </a>
            </h1>
          </div>
        </div>
      </div>
    </section>

    <NuxtPage />

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
const event = {
  "@context": "https://schema.org",
  "@type": "SportsEvent",
  name: "TREPPE HOCH 4",
  description: "Spendenlauf: Treppenlauf im Ausdauerformat",
  startDate: "2024-03-02",
  endDate: "2024-03-02",
  eventStatus: "https://schema.org/EventScheduled",
  eventAttendanceMode: "https://schema.org/OfflineEventAttendanceMode",
  location: {
    "@type": "Place",
    name: "Maritim Hotel Ulm",
    address: {
      "@type": "PostalAddress",
      streetAddress: "Basteistraße 40",
      postalCode: "89073",
      addressLocality: "Ulm",
      addressRegion: "BW",
      addressCountry: "DE",
    },
  },
  image: ["https://treppe-hoch-vier.vercel.app/treppe-hoch-vier.jpg"],
};

const formattedDate = new Date(event.startDate).toLocaleDateString("de-DE", {
  weekday: "long",
  year: "2-digit",
  month: "2-digit",
  day: "2-digit",
});

useHead({
  titleTemplate: (pageTitle) =>
    [pageTitle, event.name].filter(Boolean).join(" | "),
  viewport: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
  meta: [
    {
      name: "description",
      content: formattedDate + " @ " + event.location.name,
    },
    {
      property: "og:image",
      content: event.image[0],
    },
    { property: "og:type", content: "website" },
    { name: "twitter:card", content: "summary_large_image" },
  ],
  script: [
    {
      type: "application/ld+json",
      children: JSON.stringify(event),
    },
    {
      src: "https://plausible.io/js/script.js",
      "data-domain": "treppe-hoch-vier.de",
      defer: true,
    },
  ],
});
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
