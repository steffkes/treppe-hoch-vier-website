<template>
  <div style="background-color: #f9f9f9; min-height: 100vh">
    <section class="section">
      <div class="container is-max-desktop">
        <div class="columns">
          <div class="column is-8">
            <h1 class="title is-1 mb-6">
              <img src="/treppe-hoch-vier.svg" alt="TREPPE HOCH 4" />
            </h1>
          </div>
        </div>

        <NuxtPage />
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
