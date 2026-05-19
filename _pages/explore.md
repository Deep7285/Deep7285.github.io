---
layout: page
title: explore
permalink: /explore/
description: Life beyond the lab — places, people, rides, and things that keep me curious.
nav: true
nav_order: 8
---

<!-- Leaflet map library -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.min.css" />
<script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.min.js"></script>

<style>
#travel-map {
  height: 480px;
  width: 100%;
  border-radius: 8px;
  border: 1px solid var(--global-divider-color);
  margin: 1.5rem 0 2rem 0;
  z-index: 1;
}
.explore-section {
  margin: 2.4rem 0;
}
.explore-section h3 {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--global-theme-color);
  margin-bottom: 0.5rem;
  padding-bottom: 0.3rem;
  border-bottom: 1px solid var(--global-divider-color);
}
.explore-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  margin-top: 0.8rem;
}
.explore-gallery img {
  height: 200px;
  width: auto;
  max-width: 100%;
  object-fit: cover;
  border-radius: 6px;
  border: 1px solid var(--global-divider-color);
  cursor: zoom-in;
}
.section-divider {
  font-size: 0.74rem;
  font-weight: 600;
  letter-spacing: 0.09em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  margin: 2.8rem 0 0.8rem 0;
  padding-bottom: 0.4rem;
  border-bottom: 1px solid var(--global-divider-color);
}
.map-legend {
  font-size: 0.82rem;
  color: var(--global-text-color-light);
  margin-top: -1.2rem;
  margin-bottom: 1.8rem;
  text-align: center;
}
</style>

<p style="color: var(--global-text-color-light); font-size: 0.95rem; margin-bottom: 0.5rem;">
  Research takes you places — literally and otherwise. This page is a running record of the
  places I've been, the rides I've done, and the things outside the lab that keep me
  curious about the world. More gets added as life happens.
</p>

<!-- ============================================================ -->
<!-- INTERACTIVE TRAVEL MAP -->
<!-- ============================================================ -->

<div id="travel-map"></div>
<p class="map-legend">Click any marker for the location name. Zoom in to explore.</p>

<script>
  // Initialise map — centred between India and Europe, zoom 3
  var map = L.map('travel-map', { scrollWheelZoom: false }).setView([30, 55], 3);

  // CartoDB Positron tiles — clean, minimal, works in light and dark modes
  L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> &copy; <a href="https://carto.com/">CARTO</a>',
    subdomains: 'abcd',
    maxZoom: 19
  }).addTo(map);

  // Marker style — teal to match site theme
  var baseStyle = {
    radius: 7,
    fillColor: '#1a7a6e',
    color: '#ffffff',
    weight: 2,
    opacity: 1,
    fillOpacity: 0.85
  };

  // ── INDIA ──────────────────────────────────────────────────────
  var india = [
    { lat: 26.8467, lng: 80.9462, name: "Lucknow, Uttar Pradesh" },
    { lat: 28.6139, lng: 77.2090, name: "Delhi NCR" },
    { lat: 30.0869, lng: 78.2676, name: "Rishikesh, Uttarakhand" },
    { lat: 29.9457, lng: 78.1642, name: "Haridwar, Uttarakhand" },
    { lat: 25.3176, lng: 82.9739, name: "Varanasi, Uttar Pradesh" },
    { lat: 25.4358, lng: 81.8463, name: "Prayagraj, Uttar Pradesh" },
    { lat: 22.5726, lng: 88.3639, name: "Kolkata, West Bengal" },
    { lat: 26.9124, lng: 75.7873, name: "Jaipur, Rajasthan" },
    { lat: 23.2599, lng: 77.4126, name: "Madhya Pradesh" },
    { lat: 13.0827, lng: 80.2707, name: "Chennai, Tamil Nadu" },
    { lat:  9.2881, lng: 79.3174, name: "Rameswaram, Tamil Nadu" },
    { lat:  8.0883, lng: 77.5385, name: "Kanyakumari, Tamil Nadu" },
    { lat: 10.7870, lng: 79.1378, name: "Thanjavur, Tamil Nadu" },
    { lat:  9.9252, lng: 78.1198, name: "Madurai, Tamil Nadu" },
    { lat:  8.7642, lng: 78.1348, name: "Thoothukudi, Tamil Nadu" },
    { lat: 12.8342, lng: 79.7036, name: "Kanchipuram, Tamil Nadu" },
    { lat:  8.5241, lng: 76.9366, name: "Thiruvananthapuram, Kerala" },
    { lat: 10.5276, lng: 76.2144, name: "Thrissur, Kerala" },
    { lat: 11.6234, lng: 92.7265, name: "Andaman & Nicobar Islands" },
    { lat: 13.7199, lng: 80.2304, name: "SDSC SHAR, ISRO — Sriharikota" }
  ];

  // ── EUROPE ─────────────────────────────────────────────────────
  var europe = [
    { lat: 48.2082, lng: 16.3738, name: "Vienna, Austria" },
    { lat: 47.5623, lng: 13.6493, name: "Hallstatt, Austria" },
    { lat: 48.8566, lng:  2.3522, name: "Paris, France" },
    { lat: 41.9028, lng: 12.4964, name: "Rome, Italy" }
  ];

  // Add all markers
  india.concat(europe).forEach(function(loc) {
    L.circleMarker([loc.lat, loc.lng], baseStyle)
      .bindPopup('<strong>' + loc.name + '</strong>')
      .addTo(map);
  });
</script>

<!-- ============================================================ -->
<!-- INDIA -->
<!-- ============================================================ -->

<p class="section-divider">India</p>

<div class="explore-section">
  <h3>The South — Tamil Nadu, Kerala & Beyond</h3>
  <p>
    Four years at IIT Madras meant Chennai became a second home. From there I made my way
    through Tamil Nadu's temple towns — Thanjavur, Madurai, Kanchipuram, Rameswaram —
    and down to the very tip of the subcontinent at Kanyakumari. The Kerala coast through
    Thiruvananthapuram and Thrissur, and more recently the Andaman & Nicobar Islands.
    South India has a different pace and a completely different relationship with food,
    architecture, and water.
  </p>
  <!-- TO ADD PHOTOS: uncomment the gallery div below and fill in your image filenames
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Description" %}
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Description" %}
  </div>
  -->
</div>

<div class="explore-section">
  <h3>ISRO Campus Visit — Sriharikota</h3>
  <p>
    A visit to SDSC SHAR (Satish Dhawan Space Centre) at Sriharikota during my time at
    IIT Madras. Seeing the launch infrastructure up close — where India's space programme
    is built and launched — is one of those visits that stays with you. The scale of what
    gets done there with the resources available is genuinely remarkable.
  </p>
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/isro_1.png" class="img-fluid" alt="ISRO Sriharikota visit" %}
    {% include figure.liquid path="assets/img/isro_2.png" class="img-fluid" alt="ISRO Sriharikota visit" %}
  </div>
</div>

<div class="explore-section">
  <h3>The North & Central — UP, Uttarakhand, Rajasthan, MP</h3>
  <p>
    Home ground in many ways. Lucknow for undergrad, the Ganga towns of Varanasi and
    Prayagraj, the Himalayan foothills through Rishikesh and Haridwar. Rajasthan is a
    different India entirely — Jaipur and the different parts I've moved through have a
    texture that's hard to find anywhere else. Delhi NCR as a recurring transit and work
    point. Madhya Pradesh in between.
  </p>
  <!-- TO ADD PHOTOS: uncomment and fill in
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Description" %}
  </div>
  -->
</div>

<div class="explore-section">
  <h3>Kolkata</h3>
  <p>
    Kolkata deserves its own mention — the city has an intellectual weight and a
    relationship with literature, food, and football that doesn't exist quite the same
    way anywhere else in India. Worth every visit.
  </p>
  <!-- TO ADD PHOTOS: uncomment and fill in
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Description" %}
  </div>
  -->
</div>

<!-- ============================================================ -->
<!-- EUROPE -->
<!-- ============================================================ -->

<p class="section-divider">Europe</p>

<div class="explore-section">
  <h3>Vienna & Hallstatt, Austria</h3>
  <p>
    Vienna for THERMEC'23 — presenting my FSW research at the University of Technology
    Vienna. Arriving in Austria to present at an international conference was a full-circle
    moment from years of lab work. Hallstatt was a day trip from Vienna: a village on a
    lake in the Alps that looks like someone designed it to be photographed, and somehow
    still feels genuine despite it.
  </p>
  <!-- TO ADD PHOTOS: uncomment and fill in your Vienna/Hallstatt photos
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Vienna" %}
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Hallstatt" %}
  </div>
  -->
</div>

<div class="explore-section">
  <h3>Paris & Rome</h3>
  <p>
    Two cities that carry an enormous weight of expectation — and mostly deliver. Paris
    for its architecture and the particular way light moves across stone in the afternoon.
    Rome for the collision of two thousand years of history into a single functioning city,
    where ancient ruins sit between coffee shops and scooter traffic.
  </p>
  <!-- TO ADD PHOTOS: uncomment and fill in
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Paris" %}
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Rome" %}
  </div>
  -->
</div>

<!-- ============================================================ -->
<!-- CYCLING -->
<!-- ============================================================ -->

<p class="section-divider">On Two Wheels</p>

<div class="explore-section">
  <h3>Cycling</h3>
  <p>
    Long-distance cycling became a serious part of life during my MS at IIT Madras.
    The campus has a strong cycling culture, and the Pedal Storm event became an annual
    marker — pushing for longer distances and better times each time. Competed at PAN IIT
    cycling events with podium finishes. There's something specific about the combination
    of physical effort and distance that doesn't translate to other exercise — you actually
    go somewhere.
  </p>
  <!-- TO ADD PHOTOS: uncomment and fill in your cycling event photos
  <div class="explore-gallery">
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="IIT Madras Pedal Storm" %}
    {% include figure.liquid path="assets/img/YOUR_IMAGE.jpg" class="img-fluid" alt="Cycling event" %}
  </div>
  -->
</div>

<!-- ============================================================ -->
<!-- FOOTER NOTE -->
<!-- ============================================================ -->

<div style="margin-top: 3rem; padding-top: 1rem; border-top: 1px solid var(--global-divider-color);">
  <p style="color: var(--global-text-color-light); font-size: 0.85rem; font-style: italic;">
    This page is a work in progress — photos and places get added as I go.
    Last updated: 2025.
  </p>
</div>