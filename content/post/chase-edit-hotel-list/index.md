---
title: "The Edit by Chase Travel: Every Hotel, by Region and Country"
date: 2026-11-02
lastmod: 2026-11-02
slug: "chase-the-edit-hotel-list"
image: "togetsu-kyo-bridge.jpg"
description: "The full list of The Edit by Chase Travel hotels — 1,528 properties in 92 countries, in a single searchable, filterable table — plus how the Sapphire Reserve hotel credits and perks work."
categories: ["Travel Tips"]
tags: [chase, sapphire-reserve, the-edit, hotel-credit, hotel-list]
pinned: true
---

## What The Edit is

The Edit by Chase Travel is the curated hotel collection for Chase Sapphire Reserve, Sapphire Reserve for Business, and J.P. Morgan Reserve cardholders. You browse it inside Chase Travel, and you book through Chase Travel to get the perks.

## The perks and credits

For a prepaid stay of two or more consecutive nights at an Edit hotel, you typically get:

- Daily breakfast for two at most properties
- A property credit of about $100 (about $200 at all-inclusive properties)
- A room upgrade on arrival, when available
- Early check-in and late check-out, when available

On top of that, the Sapphire Reserve gives up to $500 a year in statement credits for Edit stays, paid as up to $250 on each of the first two qualifying bookings. As of November 2026, 177 Edit hotels also qualify for Chase's separate Select Hotels credit, so on those stays the two credits can stack to $500 on a single booking. Check the exact credit and perks for your hotel and dates in Chase Travel before you book — they vary by property.

## How to use this list

Use the search box to find a hotel, city, or country, or pick a region or country from the menus — the single table filters live, and the count below the menus tells you how many hotels match. Where we have reviewed a hotel ourselves, the **Our review** column links to our blog post and YouTube video for it. (Our MGM Grand video is a warning, not a recommendation — it is linked because it is our honest take on that hotel, same as the rest.)

## The list below

This is every Edit hotel in Chase Travel's list as compiled on November 2, 2026: **1,528 hotels in 92 countries**, in a single table with Region and Country columns, in region order. One near-duplicate pair from the source is kept as listed (two similar Nekajui Peninsula Papagayo entries in Costa Rica), so the unique-property count may be 1,527.

Hotel membership changes through the year — hotels join and leave — so confirm a hotel is still in The Edit in Chase Travel before you plan around it. This page is a reference list, not a booking site, and we are not paid by Chase or any hotel on it. The list itself comes from a third-party compilation of Chase Travel's list, not from Chase directly: Chase publishes no complete public list of its own.

<div class="hotel-filter">
<p><label>Search hotels, cities or countries: <input type="search" id="hotel-search" placeholder="e.g. Kyoto, Four Seasons, Italy"></label></p>
<p><label>Region: <select id="hotel-region"><option value="">All regions</option></select></label>
<label>Country: <select id="hotel-country"><option value="">All countries</option></select></label>
<label><input type="checkbox" id="hotel-reviewed"> Reviewed only (blog or video)</label>
<button type="button" id="hotel-reset">Clear filters</button></p>
<p id="hotel-count" aria-live="polite"></p>
<p><small>With JavaScript off, the full table below still shows; only the filtering needs JavaScript.</small></p>
</div>
<script>
/* One flat table, so filtering is just: hide/show rows. No section headings
   to hide, no per-country tables to walk — this is what makes it fast and
   reliable even at 3,000+ rows. Row text is lowercased once at load. */
document.addEventListener('DOMContentLoaded', function () {
  var search = document.getElementById('hotel-search');
  var regionSel = document.getElementById('hotel-region');
  var countrySel = document.getElementById('hotel-country');
  var reviewedBox = document.getElementById('hotel-reviewed');
  var countEl = document.getElementById('hotel-count');
  var rows = Array.prototype.slice.call(document.querySelectorAll('tr.hotel-row'));
  var total = rows.length;
  var regions = [], countries = [];
  rows.forEach(function (r) {
    r._text = r.textContent.toLowerCase();
    if (regions.indexOf(r.dataset.region) === -1) regions.push(r.dataset.region);
    if (countries.indexOf(r.dataset.country) === -1) countries.push(r.dataset.country);
  });
  regions.sort(); countries.sort();
  regions.forEach(function (x) { var o = document.createElement('option'); o.value = x; o.textContent = x; regionSel.appendChild(o); });
  countries.forEach(function (x) { var o = document.createElement('option'); o.value = x; o.textContent = x; countrySel.appendChild(o); });
  function apply() {
    var q = search.value.trim().toLowerCase();
    var reg = regionSel.value, ctry = countrySel.value, shown = 0;
    rows.forEach(function (r) {
      var ok = (!q || r._text.indexOf(q) !== -1)
        && (!reg || r.dataset.region === reg)
        && (!ctry || r.dataset.country === ctry)
        && (!reviewedBox.checked || r.dataset.reviewed === '1');
      r.style.display = ok ? '' : 'none';
      if (ok) shown++;
    });
    countEl.textContent = 'Showing ' + shown + ' of ' + total + ' hotels.';
  }
  document.getElementById('hotel-reset').addEventListener('click', function () {
    search.value = ''; regionSel.value = ''; countrySel.value = ''; reviewedBox.checked = false; apply();
  });
  search.addEventListener('input', apply);
  regionSel.addEventListener('change', apply);
  countrySel.addEventListener('change', apply);
  reviewedBox.addEventListener('change', apply);
  apply();
});
</script>

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Country</th><th>Region</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Banff Springs</td><td>Banff</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fogo Island Inn</td><td>Fogo Island</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Muir, a Luxury Collection Hotel, Halifax</td><td>Halifax</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Jasper Park Lodge</td><td>Jasper</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Chateau Lake Louise</td><td>Lake Louise</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont The Queen Elizabeth</td><td>Montreal</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Four Seasons Hotel Montreal</td><td>Montreal</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Sofitel Montreal Golden Mile</td><td>Montreal</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>The Ritz-Carlton, Montreal</td><td>Montreal</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Vogue Hotel Montreal Downtown, Curio Collection by Hilton</td><td>Montreal</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Chateau Laurier</td><td>Ottawa</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Auberge Saint-Antoine</td><td>Québec City</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Le Chateau Frontenac</td><td>Québec City</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>1 Hotel Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Four Seasons Hotel Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Park Hyatt Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Shangri-La, Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>The Ritz-Carlton, Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>The St. Regis Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>W Toronto</td><td>Toronto</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Hotel Vancouver</td><td>Vancouver</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Pacific Rim</td><td>Vancouver</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Waterfront</td><td>Vancouver</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Hyatt Vancouver Alberni Downtown</td><td>Vancouver</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Empress</td><td>Victoria</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Fairmont Chateau Whistler</td><td>Whistler</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada" data-reviewed="0"><td>Four Seasons Resort Whistler</td><td>Whistler</td><td>Canada</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Secrets Akumal Riviera Maya</td><td>Akumal</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Corazon Cabo Resort &amp; Spa</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Grand Velas Los Cabos - All Inclusive</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>ME Cabo by Meliá – Adults Only – SLH</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Montage Los Cabos</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Nobu Hotel Los Cabos</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Park Hyatt Cabo Del Sol</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The Cape, a Thompson Hotel</td><td>Cabo San Lucas</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Impression Isla Mujeres by Secrets</td><td>Cancun</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Kempinski Hotel Cancún</td><td>Cancun</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>NIZUC Resort &amp; Spa</td><td>Cancun</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>SLS Cancun</td><td>Cancun</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>SLS Playa Mujeres – ALL Inclusive Collection</td><td>Cancun</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Four Seasons Resort Tamarindo</td><td>Costalegre</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>InterContinental Presidente Cozumel Resort &amp; Spa</td><td>Cozumel</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Casa Habita, Guadalajara, a Member of Design Hotels</td><td>Guadalajara</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Unico Hotel Riviera Maya - Adults Only</td><td>Kantenah</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Four Seasons Resort Los Cabos at Costa Palmas</td><td>La Ribera</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>One&amp;Only Mandarina</td><td>Lo de Marcos</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Chable Yucatan</td><td>Mérida</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Andaz Condesa Mexico City</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Circulo Mexicano, Mexico, a Member of Design Hotels</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Condesa df, Mexico City, a Member of Design Hotels</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Four Seasons Hotel Mexico City</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Hotel Alexander</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Kimpton Virgilio Hotel</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Mondrian Mexico City Condesa</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Sofitel Mexico City Reforma</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The Ritz-Carlton Residences Mexico City</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The Ritz-Carlton, Mexico City</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The St. Regis Mexico City</td><td>Mexico City</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>InterContinental Presidente Monterrey by IHG</td><td>Monterrey</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Grand Velas Riviera Nayarit - All Inclusive</td><td>Nuevo Nayarit</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Otro Oaxaca</td><td>Oaxaca</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Alila Mayakoba</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Banyan Tree Mayakoba</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Chablé Maroma</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Fairmont Heritage Place, Mayakoba</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Grand Velas Riviera Maya - All Inclusive</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Hotel Esencia</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Impression Moxche by Secrets</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>La Casa de la Playa</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Maroma, A Belmond Hotel, Riviera Maya</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Palmaïa-The House of AïA: All Inclusive Wellness Resort</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Paradisus La Perla</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Paradisus Playa del Carmen</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The Riviera Maya EDITION at Kanai</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The St. Regis Kanai Resort, Riviera Maya</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Viceroy Riviera Maya, a Luxury Villa Resort - Adults Only</td><td>Playa del Carmen</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Banyan Tree Puebla</td><td>Puebla</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Casa Velas Adults Only All Inclusive</td><td>Puerto Vallarta</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Four Seasons Resort Punta Mita</td><td>Punta de Mita</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Naviva, A Four Seasons Resort, Punta Mita, Mexico - All Inclusive</td><td>Punta de Mita</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>The St. Regis Punta Mita Resort</td><td>Punta de Mita</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>W Punta de Mita</td><td>Punta de Mita</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Grand Velas Boutique Los Cabos</td><td>San José del Cabo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>One&amp;Only Palmilla, Los Cabos</td><td>San José del Cabo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Residences at Zadún, a Ritz-Carlton Reserve</td><td>San José del Cabo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Solaz, A Luxury Collection Resort, Los Cabos a Marriott Hotel</td><td>San José del Cabo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Viceroy Los Cabos</td><td>San José del Cabo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Zadún, a Ritz-Carlton Reserve</td><td>San José del Cabo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Casa de Sierra Nevada, A Belmond Hotel, San Miguel de Allende</td><td>San Miguel de Allende</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Hotel San Cristobal</td><td>Todos Santos</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Kimpton Mas Olas Resort and Spa</td><td>Todos Santos</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>BE Destination Tulum</td><td>Tulum</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Banyan Tree Veya Valle De Guadalupe</td><td>Valle de Guadalupe</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico" data-reviewed="0"><td>Thompson Zihuatanejo</td><td>Zihuatanejo</td><td>Mexico</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Laurel Hotel and Spa</td><td>Auburn</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Castle Hot Springs</td><td>Morristown</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Mountain Shadows Resort Scottsdale</td><td>Paradise Valley</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Phoenix Desert Ridge Resort &amp; Spa</td><td>Phoenix</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Royal Palms Resort &amp; Spa</td><td>Phoenix</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Global Ambassador</td><td>Phoenix</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Andaz Scottsdale Resort &amp; Bungalows</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Caesars Republic Scottsdale, A Hilton Hotel</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Scottsdale Princess</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Scottsdale at Troon North</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Hyatt Scottsdale Resort</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Scottsdale Camelback Inn Resort &amp; Spa</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Scottsdale Resort &amp; Spa at Montelucia</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Phoenician, a Luxury Collection Resort, Scottsdale</td><td>Scottsdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Amara Resort and Spa</td><td>Sedona</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ambiente A Landscape Hotel, Sedona</td><td>Sedona</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Enchantment Resort</td><td>Sedona</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>L&#x27;Auberge de Sedona</td><td>Sedona</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Tempe Hotel at ASU</td><td>Tempe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Canyon Ranch Tucson</td><td>Tucson</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Tucson National Resort</td><td>Tucson</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Dove Mountain</td><td>Tucson</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Anaheim Resort</td><td>Anaheim</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Westin Anaheim Resort</td><td>Anaheim</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Beverly Wilshire, Beverly Hills, A Four Seasons Hotel</td><td>Beverly Hills</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>L&#x27;Ermitage Beverly Hills</td><td>Beverly Hills</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Beverly Hills Hotel</td><td>Beverly Hills</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Maybourne Beverly Hills, Maybourne</td><td>Beverly Hills</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Peninsula Beverly Hills</td><td>Beverly Hills</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Alila Ventana Big Sur</td><td>Big Sur</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Post Ranch Inn</td><td>Big Sur</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort and Residences Napa Valley</td><td>Calistoga</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park Hyatt Aviara Resort, Golf Club &amp; Spa</td><td>Carlsbad</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Carmel Valley Ranch</td><td>Carmel</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Le Petit Pali at 8th Ave</td><td>Carmel</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Le Petit Pali at Ocean Ave</td><td>Carmel</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Bernardus Lodge &amp; Spa</td><td>Carmel Valley</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Laguna Niguel</td><td>Dana Point</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>L&#x27;Auberge Del Mar</td><td>Del Mar</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Alila Marea Beach Resort Encinitas, a Hyatt Luxury Resort</td><td>Encinitas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Farmhouse Inn</td><td>Forestville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Dawn Ranch</td><td>Guerneville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Stavrand Russian River Valley</td><td>Guerneville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Half Moon Bay</td><td>Half Moon Bay</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Healdsburg</td><td>Healdsburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Liora Estate</td><td>Healdsburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Montage Healdsburg</td><td>Healdsburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Madrona</td><td>Healdsburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hyatt Regency Huntington Beach Resort and Spa</td><td>Huntington Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Paséa Hotel &amp; Spa</td><td>Huntington Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Hyatt Indian Wells Resort &amp; Villas</td><td>Indian Wells</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Tommy Bahama Miramonte Resort &amp; Spa</td><td>Indian Wells</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Montage Laguna Beach</td><td>Laguna Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ranch at Laguna Beach</td><td>Laguna Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Lake Tahoe</td><td>Lake Tahoe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Downtown L.A. Proper</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Los Angeles at Beverly Hills</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Bel-Air - Dorchester Collection</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Per La, Autograph Collection</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental Los Angeles Downtown by IHG</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>SLS Hotel, a Luxury Collection Hotel, Beverly Hills</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Los Angeles</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W Hollywood</td><td>Los Angeles</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Malibu Beach Inn</td><td>Malibu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ranch Malibu</td><td>Malibu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Limelight Mammoth</td><td>Mammoth Lakes</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Nia, Autograph Collection</td><td>Menlo Park</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Carneros Resort and Spa</td><td>Napa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Lido House, Autograph Collection</td><td>Newport Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Newport Beach</td><td>Newport Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Resort at Pelican Hill</td><td>Newport Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Mission Pacific Beach Resort</td><td>Oceanside</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Seabird Resort</td><td>Oceanside</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ojai Valley Inn</td><td>Ojai</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Avalon Hotel &amp; Bungalows Palm Springs, a Member of Design Hotels</td><td>Palm Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ingleside Estate Hotel &amp; Bungalows- Adults Only</td><td>Palm Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Parker Palm Springs</td><td>Palm Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Palm Springs</td><td>Palm Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Silicon Valley at East Palo Alto</td><td>Palo Alto</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Nobu Hotel Palo Alto</td><td>Palo Alto</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Langham Huntington, Pasadena</td><td>Pasadena</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Rancho Mirage</td><td>Rancho Mirage</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Terranea Resort</td><td>Rancho Palos Verdes</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Inn At Rancho Santa Fe</td><td>Rancho Santa Fe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Rancho Valencia Resort and Spa</td><td>Rancho Santa Fe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Sawyer Hotel by IHG</td><td>Sacramento</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Alma San Diego Downtown, a Tribute Portfolio Hotel</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Estancia La Jolla Hotel &amp; Spa</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Grand Del Mar</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental San Diego by IHG</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kona Kai San Diego</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry San Diego</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Lodge at Torrey Pines</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The US Grant, a Luxury Collection Hotel, San Diego</td><td>San Diego</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel San Francisco</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont San Francisco</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel San Francisco</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel San Francisco at Embarcadero</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Zoe</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="1"><td>Palace Hotel, a Luxury Collection Hotel, San Francisco</td><td>San Francisco</td><td>United States</td><td>North America</td><td><a href="https://www.youtube.com/watch?v=USr5hpVl4k4">Video</a></td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>San Francisco Proper Hotel</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Taj Campton Place</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Jay, Autograph Collection</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, San Francisco</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis San Francisco</td><td>San Francisco</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>CordeValle</td><td>San Martin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>El Encanto, Santa Barbara</td><td>Santa Barbara</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Californian</td><td>Santa Barbara</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Canary Hotel by IHG</td><td>Santa Barbara</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>San Ysidro Ranch</td><td>Santa Barbara</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Bacara, Santa Barbara</td><td>Santa Barbara</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Miramar Hotel</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Casa del Mar</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Regent Santa Monica Beach</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Santa Monica Proper Hotel, a Member of Design Hotels</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Shutters on the Beach</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Pierside Santa Monica</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Viceroy Santa Monica</td><td>Santa Monica</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Cavallo Point</td><td>Sausalito</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Sonoma Mission Inn &amp; Spa</td><td>Sonoma</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Macarthur Place</td><td>Sonoma</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Lodge at Sonoma Resort, Autograph Collection</td><td>Sonoma</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Alila Napa Valley, a Hyatt Luxury Resort</td><td>St. Helena</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Auberge Du Soleil</td><td>St. Helena</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Meadowood Napa Valley</td><td>St. Helena</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Los Angeles at Westlake Village</td><td>Thousand Oaks</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel West Hollywood</td><td>West Hollywood</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton La Peer West Hollywood</td><td>West Hollywood</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sunset Marquis</td><td>West Hollywood</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sunset Tower Hotel</td><td>West Hollywood</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Sun Rose West Hollywood</td><td>West Hollywood</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The West Hollywood EDITION</td><td>West Hollywood</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Canyon Ranch Woodside</td><td>Woodside</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Bardessono Hotel and Spa</td><td>Yountville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Yountville</td><td>Yountville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Estate Yountville</td><td>Yountville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Aspen Meadows Resort</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Limelight Hotel Aspen</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>MOLLIE Aspen</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Residences at the Little Nell</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Little Nell</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Aspen Resort</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W Aspen</td><td>Aspen</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Bachelor Gulch</td><td>Avon</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park Hyatt Beaver Creek Resort &amp; Spa</td><td>Beaver Creek</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Limelight Boulder</td><td>Boulder</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Interlocken Resort</td><td>Broomfield</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Polaris</td><td>Colorado Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Denver</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Halcyon, a hotel in Cherry Creek, Denver</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Clio, a Luxury Collection Hotel, Denver Cherry Creek</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Claret Hotel by IHG</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Limelight Hotel Denver</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Crawford Hotel</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Rally Hotel at McGregor Square</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Denver</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Denver</td><td>Denver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Dunton Hot Springs</td><td>Dolores</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Gateway Canyons Resort, A Noble House Resort</td><td>Gateway</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kindred Resort a RockResort</td><td>Keystone</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Limelight Hotel Snowmass</td><td>Snowmass Village</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Viceroy Snowmass</td><td>Snowmass Village</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Viewline Resort Snowmass, Autograph Collection</td><td>Snowmass Village</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Relais &amp; Châteaux Lumière by Dunton</td><td>Telluride</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort and Residences Vail</td><td>Vail</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Hyatt Vail</td><td>Vail</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sonnenalp</td><td>Vail</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Hythe, a Luxury Collection Resort, Vail</td><td>Vail</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Sebastian - Vail</td><td>Vail</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Winvian Farm</td><td>Morris</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Quoin Hotel</td><td>Wilmington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Eaton DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Washington DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental Washington D.C. - The Wharf by IHG</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park Hyatt Washington DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Washington DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Riggs Washington DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Salamander Washington DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sofitel Washington DC Lafayette Square</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Dupont Circle Hotel</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Hay-Adams</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Jefferson</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The LINE DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Georgetown, Washington, D.C.</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Washington, D.C.</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Washington, D.C.</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Watergate Hotel</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Viceroy Washington DC</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Willard InterContinental Washington by IHG</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Yours Truly DC, Vignette Collection by IHG</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Amelia Island Resort</td><td>Amelia Island</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Amelia Island</td><td>Amelia Island</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Turnberry Resort &amp; Spa</td><td>Aventura</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Bal Harbour, Miami</td><td>Bal Harbour</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Bal Harbour Resort</td><td>Bal Harbour</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Beach Club at The Boca Raton</td><td>Boca Raton</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Cloister at The Boca Raton</td><td>Boca Raton</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Tower at The Boca Raton</td><td>Boca Raton</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Yacht Club at The Boca Raton (Adults-only)</td><td>Boca Raton</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hyatt Regency Coconut Point Resort &amp; Spa</td><td>Bonita Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Orlando at Championsgate</td><td>ChampionsGate</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Clearwater Beach Resort &amp; Spa</td><td>Clearwater Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Seagate Hotel and Spa</td><td>Delray Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hawks Cay Resort &amp; Villas</td><td>Duck Key</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel and Residences Fort Lauderdale</td><td>Fort Lauderdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Fort Lauderdale Hotel</td><td>Fort Lauderdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pelican Grand Beach Resort - A Noble House Resort</td><td>Fort Lauderdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pier Sixty Six</td><td>Fort Lauderdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W Fort Lauderdale</td><td>Fort Lauderdale</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Playa Largo Resort &amp; Spa, Autograph Collection</td><td>Key Largo</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Marquesa Key West</td><td>Key West</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ocean Key Resort - A Noble House Resort</td><td>Key West</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Oceans Edge Resort &amp; Marina</td><td>Key West</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Perry Hotel &amp; Marina</td><td>Key West</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Orlando at WALT DISNEY WORLD® Resort</td><td>Lake Buena Vista</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Little Palm Island Resort &amp; Spa</td><td>Little Torch Key</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Longboat Key Resort</td><td>Longboat Key</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Isla Bella Beach Resort &amp; Spa</td><td>Marathon</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Marco Island Beach Resort</td><td>Marco Island</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Miami</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental Miami by IHG</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton EPIC Hotel by IHG</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Mayfair House Hotel &amp; Garden - Coconut Grove Miami</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>SLS Lux Brickell</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Coconut Grove, Miami</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Key Biscayne, Miami</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Shelborne by Proper</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Trump National Doral Miami</td><td>Miami</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel South Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Andaz Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Delano Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Eden Roc Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Faena Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fontainebleau Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Loews Miami Beach Hotel</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Nobu Hotel Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>SLS South Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Lennox Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Miami Beach EDITION</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, South Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Setai, Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Standard Spa Miami Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W South Beach</td><td>Miami Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Inn on Fifth</td><td>Naples</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>LaPlaya Beach &amp; Golf Resort - A Noble House Resort</td><td>Naples</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Naples Beach Club, A Four Seasons Resort</td><td>Naples</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Naples, Tiburón</td><td>Naples</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Naples</td><td>Naples</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Orlando Bonnet Creek Resort &amp; Spa</td><td>Orlando</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Orlando, Grande Lakes</td><td>Orlando</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Lake Nona Wave Hotel</td><td>Orlando</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Orlando, Grande Lakes</td><td>Orlando</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Residences Orlando, Grande Lakes</td><td>Orlando</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Amrit Ocean Resort</td><td>Palm Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Eau Resort &amp; Spa Palm Beach</td><td>Palm Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Palm Beach</td><td>Palm Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>PGA National Resort</td><td>Palm Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ben, Autograph Collection</td><td>Palm Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Camp Creek Inn</td><td>Panama City Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Vinoy Resort &amp; Golf Club, Autograph Collection</td><td>St. Petersburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Acqualina Resort &amp; Residences On The Beach</td><td>Sunny Isles Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel at The Surf Club</td><td>Surfside</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Tampa Water Street</td><td>Tampa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Palihouse Hyde Park Village</td><td>Tampa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Tampa EDITION</td><td>Tampa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Vero Beach Hotel &amp; Spa by IHG</td><td>Vero Beach</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>FORTH Hotel Atlanta</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Atlanta</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Colee, Atlanta Buckhead, Autograph Collection</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental Buckhead Atlanta by IHG</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Shane Hotel by IHG</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Sylvan Hotel by IHG</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Loews Atlanta Hotel</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Nobu Hotel Atlanta</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Hotel At The Battery Atlanta</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Atlanta</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Atlanta</td><td>Atlanta</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Chateau Elan &amp; Winery</td><td>Braselton</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Reynolds, Lake Oconee</td><td>Greensboro</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Jekyll Ocean Club</td><td>Jekyll Island</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Bardo Savannah</td><td>Savannah</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Brice Hotel by IHG</td><td>Savannah</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Perry Lane Hotel, a Luxury Collection Hotel, Savannah</td><td>Savannah</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Savannah</td><td>Savannah</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>&#x27;Alohilani Resort Waikiki Beach</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Espacio The Jewel Of Waikiki</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Moana Surfrider, A Westin Resort &amp; Spa, Waikiki Beach</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Kahala Hotel &amp; Resort</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Laylow Waikiki, Autograph Collection</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Residences, Waikiki Beach</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Royal Hawaiian, a Luxury Collection Resort, Waikiki</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Waikiki Beach Marriott Resort &amp; Spa</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Wayfinder Waikiki</td><td>Honolulu</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton O&#x27;ahu, Turtle Bay</td><td>Kahuku</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Hualalai</td><td>Kailua-Kona</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Oahu at Ko Olina</td><td>Kapolei</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Andaz Maui at Wailea Resort</td><td>Kihei</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Kea Lani</td><td>Kihei</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Maui at Wailea</td><td>Kihei</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Wailea, Relais &amp; Châteaux</td><td>Kihei</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Wailea Beach Resort - Marriott, Maui</td><td>Kihei</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Orchid, Hawaii</td><td>Kohala Coast</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Hyatt Kauai Resort &amp; Spa</td><td>Koloa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ko&#x27;a Kea Resort on Po&#x27;ipu Beach</td><td>Koloa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Lodge at Kukui’ula</td><td>Koloa</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Lanai</td><td>Lanai</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sensei Lanai, A Four Seasons Resort</td><td>Lanai</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel Hanalei Bay</td><td>Princeville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Maui, Kapalua</td><td>West Maui</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Westin Maui Resort &amp; Spa, Ka&#x27;anapali</td><td>West Maui</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Limelight Hotel Ketchum</td><td>Ketchum</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Chicago Athletic Association, a Hyatt Hotel</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Chicago, Millennium Park</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Gray Hotel by IHG</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Loews Chicago Hotel</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Nobu Hotel Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park Hyatt Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Langham, Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Peninsula Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Viceroy Chicago</td><td>Chicago</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental Indianapolis</td><td>Indianapolis</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>21c Museum Hotel Louisville</td><td>Louisville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Genevieve</td><td>Louisville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel New Orleans</td><td>New Orleans</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Hotel Fontenot by IHG</td><td>New Orleans</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Maison Métier</td><td>New Orleans</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, New Orleans</td><td>New Orleans</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Windsor Court</td><td>New Orleans</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Virgin Hotels New Orleans</td><td>New Orleans</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hidden Pond Resort &amp; Tree Spa</td><td>Kennebunkport</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Baltimore</td><td>Baltimore</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Baltimore</td><td>Baltimore</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ivy Hotel</td><td>Baltimore</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Inn at Perry Cabin</td><td>St. Michaels</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Boston Harbor Hotel</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Copley Plaza, Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel One Dalton Street, Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Commonwealth</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Boston Hotel at the Seaport</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Parker House</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Raffles Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Langham, Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Liberty, a Marriott Luxury Collection Hotel, Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Newbury Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Boston</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>XV Beacon</td><td>Boston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Marlowe Hotel by IHG</td><td>Cambridge</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Chatham Bars Inn</td><td>Cape Cod</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Red Jacket Beach Resort</td><td>Cape Cod</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Wequassett Resort and Golf Club</td><td>Cape Cod</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Canyon Ranch Lenox</td><td>Lenox</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Inn at Hastings Park</td><td>Lexington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Wauwinet</td><td>Nantucket</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Shinola Hotel</td><td>Detroit</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Elliot Park Hotel, Autograph Collection</td><td>Minneapolis</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Minneapolis</td><td>Minneapolis</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Hotel Landing</td><td>Wayzata</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Kansas City</td><td>Kansas City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Fontaine Hotel</td><td>Kansas City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>21c Museum Hotel St Louis</td><td>St. Louis</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel St Louis</td><td>St. Louis</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Montage Big Sky</td><td>Big Sky</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>One&amp;Only Moonlight Basin</td><td>Big Sky</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Armory Hotel Bozeman by IHG</td><td>Bozeman</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Paws Up Montana</td><td>Greenough</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ranch at Rock Creek</td><td>Philipsburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Cottonwood by IHG</td><td>Omaha</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Edgewood Tahoe Resort</td><td>Lake Tahoe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>ARIA Resort &amp; Casino</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>ARIA Sky Suites</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Bellagio Hotel and Casino</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Caesars Palace</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fontainebleau Las Vegas</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Las Vegas</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Mandalay Bay Resort And Casino</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="1"><td>MGM Grand Hotel &amp; Casino</td><td>Las Vegas</td><td>United States</td><td>North America</td><td><a href="https://www.youtube.com/watch?v=Br1hcq8983A">Video</a></td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Nobu Las Vegas at Caesars Palace</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park MGM Las Vegas</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>SKYLOFTS at MGM Grand</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Cosmopolitan Las Vegas</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Reserve at Park MGM</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Vdara Hotel &amp; Spa</td><td>Las Vegas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Mount Washington Resort</td><td>Bretton Woods</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Asbury Ocean Club Hotel</td><td>Asbury Park</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Beach Plum Farm Cottages</td><td>Cape May</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Natirar</td><td>Peapack</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Rancho Encantado Santa Fe</td><td>Santa Fe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Inn and Spa at Loretto</td><td>Santa Fe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Inn of the Five Graces</td><td>Santa Fe</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Inness</td><td>Accord</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Troutbeck</td><td>Amenia</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel Brooklyn Bridge</td><td>Brooklyn</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ace Hotel Brooklyn</td><td>Brooklyn</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The William Vale</td><td>Brooklyn</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Wythe Hotel</td><td>Brooklyn</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Lake House on Canandaigua</td><td>Canandaigua</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Glenmere Mansion</td><td>Chester</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Scribner&#x27;s Catskill Lodge</td><td>Hunter</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Marram</td><td>Montauk</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Montauk Yacht Club</td><td>Montauk</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>33 Hotel, New York City, Seaport</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Baccarat Hotel New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Casa Cipriani New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Equinox Hotel New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Faena New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fouquet&#x27;s New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel New York Downtown</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Gansevoort Meatpacking</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental New York Barclay by IHG</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental New York Times Square by IHG</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>JW Marriott Essex House New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Loews Regency New York Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Lotte New York Palace</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Nine Orchard</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park Hyatt New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Park Lane New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Manhattan West</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Smyth Tribeca</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Soho Grand Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Beekman, A Thompson Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Chatwal, New York In The Unbound Collection By Hyatt</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Dominick</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Fifth Avenue Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Langham, New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The London, a Luxury Collection Hotel, New York City</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Lowell Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Mark</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ned NoMad</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Peninsula New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Plaza, a Fairmont Managed Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton New York, Central Park</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton New York, NoMad</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Standard High Line</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Standard, East Village</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Surrey, A Corinthia Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Times Square EDITION</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Towers at Lotte New York Palace</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Twenty Two New York</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Wall Street Hotel</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Whitby</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Central Park</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Virgin Hotels New York City</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W New York - Union Square</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Warren Street</td><td>New York</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Rockaway Hotel &amp; Spa</td><td>Queens</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ranch Hudson Valley</td><td>Sloatsburg, NY</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Canoe Place Inn &amp; Cottages</td><td>The Hamptons</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>EHP Resort &amp; Marina</td><td>The Hamptons</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Roundtree, Amagansett</td><td>The Hamptons</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Bohemian Lodge Asheville, Autograph Collection®</td><td>Asheville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Carolina Inn</td><td>Chapel Hill</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Tryon Park</td><td>Charlotte</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ballantyne, A Luxury Collection Hotel, Charlotte</td><td>Charlotte</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Sanderling</td><td>Duck</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Cataloochee Ranch</td><td>Maggie Valley</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Fearrington House</td><td>Pittsboro</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Cardinal Hotel by IHG</td><td>Winston-Salem</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>21C Museum Hotel Cincinnati</td><td>Cincinnati</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Cleveland</td><td>Cleveland</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel LeVeque, Autograph Collection</td><td>Columbus</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Junto</td><td>Columbus</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Oklahoma City Hotel</td><td>Oklahoma City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Black Walnut Inn &amp; Vineyard</td><td>Dundee</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Headlands Coastal Lodge &amp; Spa</td><td>Pacific City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Hotel Vintage Portland by IHG</td><td>Portland</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>RiverPlace Hotel</td><td>Portland</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Nines, a Luxury Collection Hotel, Portland</td><td>Portland</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Portland</td><td>Portland</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sunriver Resort</td><td>Sunriver</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Philadelphia at Comcast Center</td><td>Philadelphia</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Loews Philadelphia Hotel</td><td>Philadelphia</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sofitel Philadelphia at Rittenhouse Square</td><td>Philadelphia</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Rittenhouse Philadelphia</td><td>Philadelphia</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Brenton Hotel</td><td>Newport</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Castle Hill Inn</td><td>Newport</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Preserve Sporting Club &amp; Resort</td><td>Richmond</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Ocean House</td><td>Watch Hill</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Weekapaug Inn</td><td>Watch Hill</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Montage Palmetto Bluff</td><td>Bluffton</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Emeline</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Bohemian Charleston, Autograph Collection</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Bennett</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Operis, Autograph Collection®</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Charleston Place</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Pinch Hotel</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ryder Hotel</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Zero George Street Hotel</td><td>Charleston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Hilton Head Oceanfront Resort</td><td>Hilton Head Island</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Sanctuary at Kiawah Island Golf Resort</td><td>Kiawah Island</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Southall Farm &amp; Inn</td><td>Franklin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel Nashville</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Nashville</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Loews Nashville Hotel at Vanderbilt Plaza</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Noelle</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Hermitage Hotel</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Nashville, by Hyatt</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Virgin Hotels Nashville</td><td>Nashville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Austin Proper Hotel, a Member of Design Hotels</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Austin</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Austin</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Magdalena</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Van Zandt</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Lake Austin Spa Resort – All-Inclusive, Adults Only</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The LINE Austin</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Austin, by Hyatt</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W Austin</td><td>Austin</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Dallas</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hôtel Swexan</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Pittman Hotel – Downtown Dallas by IHG</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Adolphus, Autograph Collection</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Joule Dallas</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Dallas</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Dallas</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Virgin Hotels Dallas</td><td>Dallas</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Houston</td><td>Houston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Granduca Houston</td><td>Houston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Saint Augustine</td><td>Houston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Houston Grand Hotel - River Oaks</td><td>Houston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Post Oak Hotel at Uptown Houston</td><td>Houston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Houston</td><td>Houston</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton Dallas, Las Colinas</td><td>Irving</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Emma at Pearl</td><td>San Antonio</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hyatt Regency Hill Country Resort and Villas</td><td>San Antonio</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental San Antonio Riverwalk by IHG</td><td>San Antonio</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Santo San Antonio - Riverwalk by IHG</td><td>San Antonio</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson San Antonio River Walk</td><td>San Antonio</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Black Rock Mountain Resort</td><td>Heber City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Black Desert Resort</td><td>Ivins</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Grand Hyatt Deer Valley</td><td>Park City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Montage Deer Valley</td><td>Park City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Pendry Park City</td><td>Park City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Stein Eriksen Lodge</td><td>Park City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Stein Eriksen Residences</td><td>Park City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The St. Regis Deer Valley</td><td>Park City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Hotel Monaco Salt Lake City by IHG</td><td>Salt Lake City</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Snowpine Lodge</td><td>Sandy</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Sundance Mountain Resort</td><td>Sundance</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Twin Farms</td><td>Barnard</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Taconic Hotel by IHG</td><td>Manchester</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Woodstock Inn &amp; Resort</td><td>Woodstock</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Pentagon City</td><td>Arlington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton The Forum Hotel by IHG</td><td>Charlottesville</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Omni Homestead Resort</td><td>Hot Springs</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Tides Inn</td><td>Irvington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Keswick Hall &amp; Golf Club</td><td>Keswick</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Ritz-Carlton, Tysons Corner</td><td>McLean</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Salamander Middleburg</td><td>Middleburg</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Inn at Little Washington</td><td>Washington</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>InterContinental Seattle Bellevue, by IHG</td><td>Bellevue</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>1 Hotel Seattle</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Fairmont Olympic Hotel</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Hotel Seattle</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Palladian Hotel</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Lotte Hotel Seattle</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Edgewater Hotel</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The State Hotel</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Thompson Seattle</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>W Seattle</td><td>Seattle</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The American Club</td><td>Kohler</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Kimpton Journeyman Hotel by IHG</td><td>Milwaukee</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Four Seasons Resort Jackson Hole</td><td>Jackson Hole</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Hotel Terra Jackson Hole - A Noble House Resort</td><td>Jackson Hole</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Teton Mountain Lodge and Spa</td><td>Jackson Hole</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Cabins At Snake River Sporting Club</td><td>Jackson Hole</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Cloudveil, Autograph Collection</td><td>Jackson Hole</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>The Sylvan Lodge at Snake River Sporting Club</td><td>Jackson Hole</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States" data-reviewed="0"><td>Brush Creek Ranch</td><td>Saratoga</td><td>United States</td><td>North America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla" data-reviewed="0"><td>Aurora Anguilla Resort &amp; Golf Club</td><td>Anguilla</td><td>Anguilla</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla" data-reviewed="0"><td>Cap Juluca, A Belmond Hotel</td><td>Anguilla</td><td>Anguilla</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla" data-reviewed="0"><td>Four Seasons Resort and Residences Anguilla</td><td>Anguilla</td><td>Anguilla</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla" data-reviewed="0"><td>Malliouhana Resort Anguilla</td><td>Anguilla</td><td>Anguilla</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua &amp; Barbuda" data-reviewed="0"><td>Carlisle Bay</td><td>Antigua</td><td>Antigua &amp; Barbuda</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua &amp; Barbuda" data-reviewed="0"><td>Jumby Bay Island, Oetker Hotels</td><td>Antigua</td><td>Antigua &amp; Barbuda</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua &amp; Barbuda" data-reviewed="0"><td>The Inn at English Harbour</td><td>Antigua</td><td>Antigua &amp; Barbuda</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba" data-reviewed="0"><td>Hyatt Regency Aruba Resort Spa &amp; Casino</td><td>Aruba</td><td>Aruba</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba" data-reviewed="0"><td>The Ritz-Carlton, Aruba</td><td>Aruba</td><td>Aruba</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba" data-reviewed="0"><td>The St. Regis Aruba Resort</td><td>Aruba</td><td>Aruba</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>Pink Sands Resort</td><td>Eleuthera</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>The Cove Eleuthera</td><td>Eleuthera</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>Grand Hyatt Baha Mar</td><td>Nassau</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>SLS Baha Mar</td><td>Nassau</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>The Cove at Atlantis</td><td>Paradise Island</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>The Ocean Club, A Four Seasons Resort, Bahamas</td><td>Paradise Island</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas" data-reviewed="0"><td>The Reef at Atlantis</td><td>Paradise Island</td><td>Bahamas</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Barbados" data-reviewed="0"><td>Fairmont Royal Pavilion</td><td>Barbados</td><td>Barbados</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda" data-reviewed="0"><td>Hamilton Princess &amp; Beach Club - A Fairmont Hotel</td><td>Bermuda</td><td>Bermuda</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda" data-reviewed="0"><td>The Loren at Pink Beach</td><td>Bermuda</td><td>Bermuda</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda" data-reviewed="0"><td>The St. Regis Bermuda Resort</td><td>Bermuda</td><td>Bermuda</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands" data-reviewed="0"><td>Grand Hyatt Grand Cayman Resort &amp; Spa</td><td>Grand Cayman</td><td>Cayman Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands" data-reviewed="0"><td>Hotel Indigo Grand Cayman</td><td>Grand Cayman</td><td>Cayman Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands" data-reviewed="0"><td>Kimpton Seafire Resort + Spa by IHG</td><td>Grand Cayman</td><td>Cayman Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands" data-reviewed="0"><td>The Ritz-Carlton, Grand Cayman</td><td>Grand Cayman</td><td>Cayman Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands" data-reviewed="0"><td>The Westin Grand Cayman Seven Mile Beach Resort &amp; Spa</td><td>Grand Cayman</td><td>Cayman Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominica" data-reviewed="0"><td>Intercontinental Dominica Cabrits Resort &amp; Spa</td><td>Dominica</td><td>Dominica</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>Casa de Campo Resort and Villas</td><td>La Romana</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>Eden Roc Cap Cana</td><td>Punta Cana</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>Paradisus Palma Real Golf &amp; Spa Resort All Inclusive</td><td>Punta Cana</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>The St. Regis Cap Cana Resort</td><td>Punta Cana</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>Tortuga Bay Hotel</td><td>Punta Cana</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>Zel Punta Cana All Suites</td><td>Punta Cana</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic" data-reviewed="0"><td>Kimpton Las Mercedes by IHG</td><td>Santo Domingo</td><td>Dominican Republic</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada" data-reviewed="0"><td>Calabash Hotel</td><td>Grenada</td><td>Grenada</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada" data-reviewed="0"><td>Six Senses La Sagesse Grenada</td><td>Grenada</td><td>Grenada</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica" data-reviewed="0"><td>Half Moon</td><td>Montego Bay</td><td>Jamaica</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica" data-reviewed="0"><td>Round Hill Hotel &amp; Villas</td><td>Montego Bay</td><td>Jamaica</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica" data-reviewed="0"><td>S Hotel Montego Bay</td><td>Montego Bay</td><td>Jamaica</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico" data-reviewed="0"><td>Dorado Beach, a Ritz-Carlton Reserve</td><td>Dorado</td><td>Puerto Rico</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico" data-reviewed="0"><td>Residences at Dorado Beach, a Ritz-Carlton Reserve</td><td>Dorado</td><td>Puerto Rico</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico" data-reviewed="0"><td>Four Seasons Resort and Residences Puerto Rico</td><td>Río Grande</td><td>Puerto Rico</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico" data-reviewed="0"><td>Condado Vanderbilt Hotel</td><td>San Juan</td><td>Puerto Rico</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico" data-reviewed="0"><td>Fairmont El San Juan Hotel</td><td>San Juan</td><td>Puerto Rico</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy" data-reviewed="0"><td>Fouquet&#x27;s Saint-Barth</td><td>St. Barthelemy</td><td>St. Barthélemy</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy" data-reviewed="0"><td>Hotel Le Toiny</td><td>St. Barthelemy</td><td>St. Barthélemy</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy" data-reviewed="0"><td>Le Barthélemy Hotel &amp; Spa</td><td>St. Barthelemy</td><td>St. Barthélemy</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy" data-reviewed="0"><td>Le Sereno</td><td>St. Barthelemy</td><td>St. Barthélemy</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Kitts &amp; Nevis" data-reviewed="0"><td>Four Seasons Resort - Nevis</td><td>St. Kitts &amp; Nevis</td><td>St. Kitts &amp; Nevis</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Kitts &amp; Nevis" data-reviewed="0"><td>Park Hyatt St. Kitts</td><td>St. Kitts &amp; Nevis</td><td>St. Kitts &amp; Nevis</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Lucia" data-reviewed="0"><td>Cap Maison Resort &amp; Spa</td><td>St. Lucia</td><td>St. Lucia</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Lucia" data-reviewed="0"><td>Sugar Beach, A Viceroy Resort</td><td>St. Lucia</td><td>St. Lucia</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Lucia" data-reviewed="0"><td>Zoetry Marigot Bay St. Lucia</td><td>St. Lucia</td><td>St. Lucia</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Martin" data-reviewed="0"><td>La Samanna, A Belmond Hotel, St. Martin</td><td>St. Martin</td><td>St. Martin</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>COMO Parrot Cay</td><td>Parrot Cay</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>Beach Enclave</td><td>Providenciales</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>Grace Bay Club</td><td>Providenciales</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>Rock House</td><td>Providenciales</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>South Bank</td><td>Providenciales</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>The Ritz-Carlton, Turks &amp; Caicos</td><td>Providenciales</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>Wymara Resort and Villas</td><td>Providenciales</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands" data-reviewed="0"><td>Salterra, a Luxury Collection Resort &amp; Spa, South Caicos</td><td>South Caicos</td><td>Turks &amp; Caicos Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands" data-reviewed="0"><td>Buoy Haus Beach Resort St. Thomas, Autograph Collection</td><td>St. Thomas</td><td>U.S. Virgin Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands" data-reviewed="0"><td>The Ritz-Carlton, St. Thomas</td><td>St. Thomas</td><td>U.S. Virgin Islands</td><td>Caribbean</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina" data-reviewed="0"><td>Faena Hotel Buenos Aires</td><td>Buenos Aires</td><td>Argentina</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina" data-reviewed="0"><td>Four Seasons Hotel Buenos Aires</td><td>Buenos Aires</td><td>Argentina</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina" data-reviewed="0"><td>Palacio Duhau - Park Hyatt Buenos Aires</td><td>Buenos Aires</td><td>Argentina</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina" data-reviewed="0"><td>Awasi Iguazú</td><td>Puerto Iguazú</td><td>Argentina</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina" data-reviewed="0"><td>The Vines Resort &amp; Spa</td><td>Uco Valley</td><td>Argentina</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize" data-reviewed="0"><td>Alaia Belize, Autograph Collection</td><td>Ambergris Caye</td><td>Belize</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize" data-reviewed="0"><td>Itz’ana Resort &amp; Residences, Placencia</td><td>Placencia</td><td>Belize</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil" data-reviewed="0"><td>Hotel das Cataratas, A Belmond Hotel, Iguassu Falls</td><td>Foz do Iguaçu</td><td>Brazil</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil" data-reviewed="0"><td>Copacabana Palace, A Belmond Hotel, Rio de Janeiro</td><td>Rio de Janeiro</td><td>Brazil</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil" data-reviewed="0"><td>Fairmont Rio de Janeiro Copacabana</td><td>Rio de Janeiro</td><td>Brazil</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil" data-reviewed="0"><td>Santa Teresa Hotel Rio de Janeiro - MGallery Collection</td><td>Rio de Janeiro</td><td>Brazil</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil" data-reviewed="0"><td>InterContinental São Paulo by IHG</td><td>São Paulo</td><td>Brazil</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil" data-reviewed="0"><td>Palacio Tangara, Oetker Hotels</td><td>São Paulo</td><td>Brazil</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile" data-reviewed="0"><td>The Ritz-Carlton, Santiago</td><td>Santiago</td><td>Chile</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia" data-reviewed="0"><td>Four Seasons Hotel Bogota</td><td>Bogotá</td><td>Colombia</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia" data-reviewed="0"><td>Four Seasons Hotel Bogotá Casa Medina</td><td>Bogotá</td><td>Colombia</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia" data-reviewed="0"><td>Casa Pestagua Relais Châteaux</td><td>Cartagena</td><td>Colombia</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia" data-reviewed="0"><td>InterContinental Cartagena De Indias by IHG</td><td>Cartagena</td><td>Colombia</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia" data-reviewed="0"><td>Sofitel Legend Santa Clara Cartagena</td><td>Cartagena</td><td>Colombia</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia" data-reviewed="0"><td>Sofitel Barú Cartagena Beach Resort</td><td>Cartagena de Indias</td><td>Colombia</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Nayara Gardens</td><td>La Fortuna</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Nayara Springs - Adults only</td><td>La Fortuna</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Nayara Tented Camp</td><td>La Fortuna</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Tabacón Thermal Resort &amp; Spa</td><td>La Fortuna</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Los Altos Resort</td><td>Manuel Antonio</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Nekajui Peninsula Papagayo, a Ritz-Carlton Reserve Residence</td><td>Papagayo</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Andaz Peninsula Papagayo Resort, Costa Rica</td><td>Peninsula Papagayo</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Four Seasons Resort Peninsula Papagayo, Costa Rica</td><td>Peninsula Papagayo</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Nekajui Peninsula Papagayo, a Ritz-Carlton Reserve</td><td>Peninsula Papagayo</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>W Costa Rica - Reserva Conchal</td><td>Playa Conchal</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica" data-reviewed="0"><td>Hotel Nantipa - A Tico Beach Experience</td><td>Santa Teresa</td><td>Costa Rica</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Honduras" data-reviewed="0"><td>Kimpton Grand Roatan Resort And Spa by IHG</td><td>Roatán</td><td>Honduras</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama" data-reviewed="0"><td>Sofitel Legend Casco Viejo, Panama City</td><td>Panama City</td><td>Panama</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama" data-reviewed="0"><td>The Santa Maria, a Luxury Collection Hotel &amp; Golf Resort, Panama City</td><td>Panama City</td><td>Panama</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru" data-reviewed="0"><td>Las Casitas, A Belmond Hotel</td><td>Arequipa</td><td>Peru</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru" data-reviewed="0"><td>Monasterio, A Belmond Hotel, Cusco</td><td>Cusco</td><td>Peru</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru" data-reviewed="0"><td>Palacio Nazarenas, A Belmond Hotel, Cusco</td><td>Cusco</td><td>Peru</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru" data-reviewed="1"><td>Rio Sagrado, A Belmond Hotel, Sacred Valley</td><td>Cusco</td><td>Peru</td><td>Central &amp; South America</td><td><a href="https://www.youtube.com/watch?v=ZsNwOFKryvw">Video</a></td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru" data-reviewed="0"><td>Sanctuary Lodge, A Belmond Hotel, Machu Picchu</td><td>Cusco</td><td>Peru</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru" data-reviewed="0"><td>Miraflores Park, A Belmond Hotel, Lima</td><td>Lima</td><td>Peru</td><td>Central &amp; South America</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>Hotel Goldener Hirsch, a Luxury Collection Hotel, Salzburg</td><td>Salzburg</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>Almanac Palais Vienna</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>Anantara Palais Hansen Vienna Hotel</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>Hotel Imperial, a Luxury Collection Hotel, Vienna</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>Hotel Sacher Wien</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>Park Hyatt Vienna</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>SO/ Vienna</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>The Amauris Vienna - Relais &amp; Châteaux</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria" data-reviewed="0"><td>The Ritz-Carlton, Vienna</td><td>Vienna</td><td>Austria</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium" data-reviewed="0"><td>Botanic Sanctuary Antwerp - The Leading Hotels of the World</td><td>Antwerp</td><td>Belgium</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium" data-reviewed="0"><td>Corinthia Grand Hotel Astoria, Brussels</td><td>Brussels</td><td>Belgium</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium" data-reviewed="0"><td>Hotel Amigo, a Rocco Forte hotel</td><td>Brussels</td><td>Belgium</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium" data-reviewed="0"><td>Le Louise Hotel Brussels - MGallery</td><td>Brussels</td><td>Belgium</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium" data-reviewed="0"><td>Sofitel Brussels Europe</td><td>Brussels</td><td>Belgium</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia" data-reviewed="0"><td>Sun Gardens Dubrovnik</td><td>Dubrovnik</td><td>Croatia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia" data-reviewed="0"><td>Villa Dubrovnik</td><td>Dubrovnik</td><td>Croatia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia" data-reviewed="0"><td>Maslina Resort</td><td>Hvar</td><td>Croatia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia" data-reviewed="0"><td>Grand Hotel Brioni Pula A Radisson Collection Hotel</td><td>Pula</td><td>Croatia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia" data-reviewed="0"><td>Radisson Blu Resort &amp; Spa, Split</td><td>Split</td><td>Croatia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Cyprus" data-reviewed="0"><td>Parklane, a Luxury Collection Resort &amp; Spa, Limassol</td><td>Limassol</td><td>Cyprus</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czechia" data-reviewed="0"><td>Andaz Prague</td><td>Prague</td><td>Czechia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czechia" data-reviewed="0"><td>Augustine, a Luxury Collection Hotel, Prague</td><td>Prague</td><td>Czechia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czechia" data-reviewed="0"><td>Four Seasons Hotel Prague</td><td>Prague</td><td>Czechia</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark" data-reviewed="0"><td>NH Collection Copenhagen</td><td>Copenhagen</td><td>Denmark</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark" data-reviewed="0"><td>Nimb Hotel</td><td>Copenhagen</td><td>Denmark</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark" data-reviewed="0"><td>Nobis Hotel Copenhagen, a Member of Design Hotels</td><td>Copenhagen</td><td>Denmark</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Finland" data-reviewed="0"><td>Hotel NH Collection Helsinki Grand Hansa</td><td>Helsinki</td><td>Finland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Château de Fonscolombe</td><td>Aix-en-Provence</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Villa Gallici Hôtel &amp; Spa - Relais &amp; Châteaux</td><td>Aix-en-Provence</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>La Mirande</td><td>Avignon</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Fleur de Loire</td><td>Blois</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Capelongue, a Beaumier Hotel</td><td>Bonnieux</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>InterContinental Bordeaux - Le Grand Hotel</td><td>Bordeaux</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Mondrian Bordeaux Les Carmes</td><td>Bordeaux</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Carlton Cannes, a Regent Hotel</td><td>Cannes</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Five Seas by Inwood Hotels</td><td>Cannes</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Hôtel Barrière Le Majestic Cannes</td><td>Cannes</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Hotel Martinez</td><td>Cannes</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Mondrian Cannes</td><td>Cannes</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Château De Berne</td><td>Flayosc</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Domaine de Primard</td><td>Guainville</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>InterContinental Chantilly Chateau Mont Royal by IHG</td><td>La Chapelle-en-Serval</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Coquillade Provence</td><td>Luberon</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Domaine de Fontenille</td><td>Luberon</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Cour des Loges Lyon, A Radisson Collection Hotel</td><td>Lyon</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>InterContinental Lyon - Hotel Dieu</td><td>Lyon</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>InterContinental Marseille - Hotel Dieu by IHG</td><td>Marseille</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Four Seasons Resort Megeve</td><td>Megève</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Anantara Plaza Nice Hotel</td><td>Nice</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Hotel Du Couvent, A Luxury Collection Hotel, Nice, France</td><td>Nice</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Bulgari Hotel Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Castille Paris – Starhotels Collezione</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Cheval Blanc Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Fauchon L&#x27;Hotel Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Four Seasons Hotel George V</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Grand Hôtel du Palais Royal</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Hotel Balzac Paris &amp; Spa Ikoï</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Hôtel Fouquet&#x27;s Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Hôtel Plaza Athénée - Dorchester Collection</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>InterContinental Paris le Grand</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>J.K. Place Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Kimpton St Honore Paris by IHG</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>La Fantaisie</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>La Reserve Paris Hotel and Spa</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Le Bristol Paris, Oetker Hotels</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Le Meurice - Dorchester Collection</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Le Royal Monceau - Raffles Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Maison Delano Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Park Hyatt Paris-Vendôme</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Pavillon de la Reine &amp; Spa, Place des Vosges</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Pavillon Faubourg Saint-Germain</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Relais Christine</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Ritz Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Saint James Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Shangri-La Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>SO/ Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Sofitel Paris Baltimore Tour Eiffel Hotel</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Sofitel Paris Le Faubourg</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>The Peninsula Paris</td><td>Paris</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>COMO Le Montrachet</td><td>Puligny-Montrachet</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Monte-Carlo Beach Hotel</td><td>Roquebrune-Cap-Martin</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>The Maybourne Riviera, Maybourne</td><td>Roquebrune-Cap-Martin</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France" data-reviewed="0"><td>Grand-Hôtel du Cap-Ferrat, A Four Seasons Hotel</td><td>Saint-Jean-Cap-Ferrat</td><td>France</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Brenners Park-Hotel &amp; Spa, Oetker Hotels</td><td>Baden-Baden</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Das Stue</td><td>Berlin</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Hotel De Rome Berlin</td><td>Berlin</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Regent Berlin</td><td>Berlin</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>The Ritz-Carlton, Berlin</td><td>Berlin</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Excelsior Hotel Ernst am Dom</td><td>Cologne</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Kimpton Main Frankfurt by IHG</td><td>Frankfurt</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Sofitel Frankfurt Opera</td><td>Frankfurt</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Fairmont Hotel Vier Jahreszeiten Hamburg</td><td>Hamburg</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Koenigshof, A Luxury Collection Hotel, Munich</td><td>Munich</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Rocco Forte The Charles Hotel</td><td>Munich</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany" data-reviewed="0"><td>Sofitel Munich Bayerpost</td><td>Munich</td><td>Germany</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Domes of Elounda, Autograph Collection</td><td>Agios Nikolaos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Elounda Mare Relais &amp; Chateaux Hotel</td><td>Agios Nikolaos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>InterContinental Crete by IHG</td><td>Agios Nikolaos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Minos Beach Art Hotel</td><td>Agios Nikolaos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Phāea Blue - Small Luxury Hotels of the World</td><td>Agios Nikolaos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Academias Hotel, Autograph Collection</td><td>Athens</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Athenaeum InterContinental by IHG</td><td>Athens</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Athens Capital Center Hotel</td><td>Athens</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Hotel Grande Bretagne, a Luxury Collection Hotel, Athens</td><td>Athens</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>King George, a Luxury Collection Hotel, Athens</td><td>Athens</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>New Hotel</td><td>Athens</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Domes Noruz Chania, Autograph Collection - Adults Only</td><td>Chania</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Domes Zeen Chania, a Luxury Collection Resort, Crete</td><td>Chania</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>The Romanos, a Luxury Collection Resort, Costa Navarino</td><td>Costa Navarino</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>W Costa Navarino</td><td>Costa Navarino</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>One&amp;Only Aesthesis</td><td>Glyfada</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>The Danai</td><td>Halkidiki</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Amirandes, Grecotel Boutique Resort</td><td>Heraklion</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Phāea Cretan Malia, a Member of Design Hotels</td><td>Hersonissos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>One&amp;Only Kéa Island</td><td>Kea</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Bill &amp; Coo Mykonos</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Deos Mykonos</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Kouros Hotel &amp; Suites</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Myconian Ambassador Hotel Relais &amp; Chateaux</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Myconian Kyma, a member of Design Hotels</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Myconian Villa Collection</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Mykonos Blu, A Grecotel Resort to Live</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Mykonos Grand Hotel &amp; Resort</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Santa Marina, a Luxury Collection Resort, Mykonos</td><td>Mykonos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Avant Mar</td><td>Naousa Paros</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Cosme, A Luxury Collection Resort, Paros</td><td>Paros</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Parilio, a Member of Design Hotels</td><td>Paros</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Andronis Minois</td><td>Paros Island</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Caramel, Grecotel Boutique Resort</td><td>Rethymno</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Canaves Epitome - Small Luxury Hotels of the World</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Canaves Oia Suites - Small Luxury Hotels of the World</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Katikies Garden Santorini - The Leading Hotels Of The World</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Katikies Santorini - The Leading Hotels of the world</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Katikies Santorini – Pelagos House - The Leading Hotels of the World</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Magma Resort Santorini, part of The Unbound Collection by Hyatt</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Mystique, a Luxury Collection Hotel, Santorini</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Nobu Hotel Santorini</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>NOŪS Santorini</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Santo Pure Oia Suites &amp; Villas</td><td>Santorini</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Euphoria Retreat, Mystras</td><td>Sparta</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Four Seasons Astir Palace Hotel Athens</td><td>Vari-Voula-Vouliagmeni</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece" data-reviewed="0"><td>Olea All Suite Hotel, a Member of Design Hotels</td><td>Zakynthos</td><td>Greece</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Al Habtoor Palace Budapest, Preferred Hotels &amp; Resorts</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Anantara New York Palace Budapest - A Leading Hotel of the World</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Corinthia Budapest</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Dorothea Hotel, Budapest, Autograph Collection</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Four Seasons Gresham Palace</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Kimpton BEM Budapest by IHG</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary" data-reviewed="0"><td>Párisi Udvar Hotel Budapest</td><td>Budapest</td><td>Hungary</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Iceland" data-reviewed="0"><td>The Reykjavik EDITION</td><td>Reykjavik</td><td>Iceland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Adare Manor</td><td>Adare</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Ballyfin Demesne</td><td>Ballyfin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Ashford Castle</td><td>Cong</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>The Lodge at Ashford Castle</td><td>Cong</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>The River Lee Hotel</td><td>Cork</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Anantara The Marker Hotel Dublin Hotel</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Dylan Hotel</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>InterContinental Dublin by IHG</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>The Fitzwilliam Hotel</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>The Merrion Hotel</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>The Shelbourne, Autograph Collection</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>The Westbury Dublin</td><td>Dublin</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Glenlo Abbey Hotel</td><td>Galway</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Park Hotel Kenmare</td><td>Kenmare</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Carton House, A Fairmont Hotel</td><td>Maynooth</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland" data-reviewed="0"><td>Dromoland Castle</td><td>Newmarket-on-Fergus</td><td>Ireland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Caruso, A Belmond Hotel, Amalfi Coast</td><td>Amalfi Coast</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Casa Angelina</td><td>Amalfi Coast</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Villa Franca Positano</td><td>Amalfi Coast</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Il San Pietro di Positano</td><td>Amalfi Coast</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Santa Caterina</td><td>Amalfi Coast</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa La Massa</td><td>Bagno a Ripoli</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>COMO Castello Del Nero</td><td>Barberino Tavarnelle</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Quisisana</td><td>Capri</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel La Palma, Oetker Hotels</td><td>Capri</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>J.K. Place Capri</td><td>Capri</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Jumeirah Capri Palace</td><td>Capri</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa Marina Capri Hotel &amp; Spa</td><td>Capri</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Ancora Cortina</td><td>Cortina d&#x27;Ampezzo</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Savoia Cortina d&#x27;Ampezzo, A Radisson Collection Hotel</td><td>Cortina d&#x27;Ampezzo</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>7Pines Resort Sardinia</td><td>Costa Smeralda</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Cala di Volpe, a Luxury Collection Hotel, Costa Smeralda</td><td>Costa Smeralda</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>CPH Pevero Hotel</td><td>Costa Smeralda</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Romazzino, A Belmond Hotel, Costa Smeralda</td><td>Costa Smeralda</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Courmayeur Montblanc by R Collection Hotels</td><td>Courmayeur</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Borgo Egnazia</td><td>Fasano</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte Masseria Torre Maizza</td><td>Fasano</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa San Michele, A Belmond Hotel, Florence</td><td>Fiesole</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Four Seasons Hotel Firenze</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Helvetia &amp; Bristol Firenze – Starhotels Collezione</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Lungarno - Lungarno Collection</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Regency, Florence</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>IL Tornabuoni, part of the Unbound Collection by Hyatt</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Portrait Firenze - Lungarno Collection</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte Hotel Savoy</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Sina Villa Medici, Autograph Collection</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The Excelsior, a Luxury Collection Hotel, Florence</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The Place Firenze</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The St. Regis Florence</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa Cora</td><td>Florence</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Tremezzo, Lake Como</td><td>Lake Como</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Victoria Concept &amp; Spa, by R Collection Hotels</td><td>Lake Como</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Il Sereno Lake Como</td><td>Lake Como</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Palazzo Venezia</td><td>Lake Como</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Passalacqua</td><td>Lake Como</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa d&#x27;Este</td><td>Lake Como</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Lefay Resort &amp; SPA Lago Di Garda</td><td>Lake Garda</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Casa di Langa</td><td>Langhe</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Il Santavenere</td><td>Maratea</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Bulgari Hotel Milano</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Casa Brera, a Luxury Collection Hotel, Milan</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Casa Cipriani Milano</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Four Seasons Hotel Milano</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel et de Milan</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Principe Di Savoia</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>ME Milan il Duca</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Palazzo Touring Club Milan, A Radisson Collection Hotel</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Park Hyatt Milan</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Portrait Milano - Lungarno Collection</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte House, Milan</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Straf, Milan, a Member Of Design Hotels</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The Carlton, Milan, a Rocco Forte Hotel</td><td>Milan</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Castelfalfi</td><td>Montaione</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Castello Banfi - Il Borgo - Relais et Chateaux</td><td>Montalcino</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Il San Corrado di Noto Luxury Resort</td><td>Noto</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte Villa Igiea</td><td>Palermo</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Lefay Resort &amp; SPA Dolomiti</td><td>Pinzolo</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>La Roqqa</td><td>Porto Ercole</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Splendido Mare, A Belmond Hotel, Portofino</td><td>Portofino</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Splendido, A Belmond Hotel, Portofino</td><td>Portofino</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Pieve Aldina</td><td>Radda in Chianti</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Anantara Palazzo Naiadi Rome Hotel - A Leading Hotel of the World</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Baglioni Hotel Regina - The Leading Hotels of the World</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Bulgari Hotel Roma</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Casa Monti Roma</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Corinthia Rome</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Eden - Dorchester Collection</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Maalot Roma</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Splendide Royal - The Leading Hotels of the World</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>InterContinental Rome Ambasciatori Palace</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>J.K. Place Roma</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Palazzo Ripetta</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Portrait Roma</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte Hotel de la Ville</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte Hotel De Russie</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Six Senses Rome</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Sofitel Roma Villa Borghese</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The Rome EDITION</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The St. Regis Rome</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa Agrippina a Gran Melia Hotel</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>W Rome</td><td>Rome</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Terme di Saturnia Natural Spa &amp; Golf Resort</td><td>Saturnia</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Rocco Forte Private Villas</td><td>Sciacca</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Verdura Resort</td><td>Sciacca</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Borgo San Felice Resort</td><td>Siena</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Castello di Casole, A Belmond Hotel, Tuscany</td><td>Siena</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Continental Siena – Starhotels Collezione</td><td>Siena</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Le Fontanelle</td><td>Siena</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Excelsior Vittoria</td><td>Sorrento</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Grand Hotel Timeo, A Belmond Hotel, Taormina</td><td>Taormina</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Mazzaro&#x27; Sea Palace - VRetreats</td><td>Taormina</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>San Domenico Palace, Taormina, A Four Seasons Hotel</td><td>Taormina</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The Ashbee Hotel</td><td>Taormina</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Villa Sant&#x27;Andrea, A Belmond Hotel, Taromina Mare</td><td>Taormina</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Gardena Grödnerhof Hotel &amp; Spa</td><td>Val Gardena</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Baglioni Hotel Luna - The Leading Hotels of the World</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Ca&#x27; di Dio</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Hotel Cipriani, A Belmond Hotel, Venice</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Londra Palace Venezia</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>Radisson Collection Palazzo Nani, Venice</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The Gritti Palace, a Luxury Collection Hotel, Venice</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy" data-reviewed="0"><td>The St. Regis Venice</td><td>Venice</td><td>Italy</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Malta" data-reviewed="0"><td>Iniala Valletta</td><td>Malta</td><td>Malta</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Malta" data-reviewed="0"><td>InterContinental Malta by IHG</td><td>Malta</td><td>Malta</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco" data-reviewed="0"><td>Fairmont Monte Carlo</td><td>Monaco</td><td>Monaco</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco" data-reviewed="0"><td>Hotel de Paris Monte-Carlo</td><td>Monaco</td><td>Monaco</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco" data-reviewed="0"><td>Hotel Hermitage Monte-Carlo</td><td>Monaco</td><td>Monaco</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro" data-reviewed="0"><td>One&amp;Only Portonovi</td><td>Bay of Kotor</td><td>Montenegro</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro" data-reviewed="0"><td>The Chedi Lustica Bay</td><td>Bay of Kotor</td><td>Montenegro</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Anantara Grand Hotel Krasnapolsky Amsterdam</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Andaz Amsterdam, Prinsengracht, by Hyatt</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>De L&#x27;Europe Amsterdam</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>InterContinental Amstel Amsterdam by IHG</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Kimpton De Witt Amsterdam by IHG</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Mandarin Oriental Conservatorium, Amsterdam</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Pillows Grand Boutique Hotel Maurits at the Park</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Pulitzer Amsterdam</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Sofitel Legend The Grand Amsterdam</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>The Dylan Amsterdam</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands" data-reviewed="0"><td>Tivoli Doelen Amsterdam Hotel</td><td>Amsterdam</td><td>Netherlands</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Norway" data-reviewed="0"><td>Sommerro</td><td>Oslo</td><td>Norway</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Poland" data-reviewed="0"><td>Nobu Hotel Warsaw</td><td>Warsaw</td><td>Poland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Poland" data-reviewed="0"><td>Raffles Europejski Warsaw</td><td>Warsaw</td><td>Poland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Kimpton Atlântico Algarve by IHG</td><td>Albufeira</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Pine Cliffs Ocean Suites, a Luxury Collection Resort &amp; Spa</td><td>Albufeira</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>W Algarve</td><td>Albufeira</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>W Residences Algarve</td><td>Albufeira</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Octant Furnas</td><td>Azores</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Octant Ponta Delgada</td><td>Azores</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Herdade da Malhadinha Nova</td><td>Beja</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Octant Praia Verde</td><td>Castro Marim</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Octant Douro</td><td>Douro Valley</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Six Senses Douro Valley</td><td>Douro Valley</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Andaz Lisbon</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Bairro Alto Hotel - The Leading Hotels of the World</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Convent Square Lisbon, Vignette Collection by IHG</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Corinthia Lisbon</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Four Seasons Hotel Ritz Lisbon</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>InterContinental Lisbon by IHG</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>The One Palácio da Anunciada</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Tivoli Avenida Liberdade Lisboa – A Leading hotel of the world</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Valverde Lisboa Hotel &amp; Garden</td><td>Lisbon</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Viceroy at Ombria Algarve</td><td>Loulé</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Reids Palace, A Belmond Hotel, Madeira</td><td>Madeira</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Savoy Palace</td><td>Madeira</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Vermelho Melides - Relais &amp; Châteaux</td><td>Melides</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>L&#x27;And Vineyards</td><td>Montemor-o-Novo</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Octant Vila Monte</td><td>Olhão</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Bela Vista Hotel &amp; SPA - Relais &amp; Châteaux</td><td>Portimão</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Casa da Companhia Hotel &amp; Spa, Vignette Collection by IHG</td><td>Porto</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>InterContinental Porto-Palacio das Cardosas</td><td>Porto</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>The Largo</td><td>Porto</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal" data-reviewed="0"><td>Penha Longa Resort</td><td>Sintra</td><td>Portugal</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Romania" data-reviewed="0"><td>Corinthia Grand Hotel du Boulevard Bucharest</td><td>Bucharest</td><td>Romania</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Es Racó d’Artà, a Member of Design Hotels™</td><td>Arta</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Son Bunyola Hotel</td><td>Banyalbufar</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Almanac Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Grand Hyatt Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Arts Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel El Palace Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Neri Relais &amp; Chateaux</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>InterContinental Barcelona by IHG</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Kimpton Vividora Hotel by IHG</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Majestic Hotel &amp; Spa Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>ME Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Nobu Hotel Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Serras Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Barcelona EDITION</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The One Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>W Barcelona</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>WITTMORE HOTEL - Adults Only</td><td>Barcelona</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Radisson Collection Bilbao</td><td>Bilbao</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel de Mar a Gran Melia Hotel</td><td>Calvia</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Kimpton Aysla Mallorca by IHG</td><td>Calvia</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The St. Regis Mardavall Mallorca Resort</td><td>Calvia</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Cap Vermell Grand Hotel</td><td>Canyamel</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Finca Cortesin Hotel Golf &amp; Spa</td><td>Casares</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hospes Palacio del Bailio</td><td>Córdoba</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>La Residencia, A Belmond Hotel, Mallorca</td><td>Deia</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Marqués de Riscal, a Luxury Collection Hotel, Elciego</td><td>Elciego</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Seda Club Hotel – Small Luxury Hotel</td><td>Granada</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>BLESS Ibiza Cala Nova</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>ME Ibiza</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Mondrian Ibiza</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Nobu Hotel Ibiza Bay</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Petunia Ibiza, a Beaumier Hotel</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Six Senses Ibiza</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Standard, Ibiza</td><td>Ibiza</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Bless Hotel Madrid</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Casa de las Artes, The Melia Collection</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Four Seasons Hotel Madrid</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Gran Hotel Inglés - The Leading Hotels of the World</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Fenix, a Gran Meliá Hotel</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>InterContinental Madrid by IHG</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Palacio de los Duques Gran Meliá - The Leading Hotels of the World</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Santo Mauro, a Luxury Collection Hotel</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Madrid EDITION</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Palace, a Luxury Collection Hotel, Madrid</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Principal Madrid, Small Luxury Hotels</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Thompson Madrid, by Hyatt</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>URSO Hotel &amp; Spa</td><td>Madrid</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Palacio Solecio, a Small Luxury Hotel of the World</td><td>Málaga</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Kimpton Los Monteros Marbella</td><td>Marbella</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Marbella Club Hotel Golf Resort &amp; Spa</td><td>Marbella</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Nobu Hotel Marbella</td><td>Marbella</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Villa Le Blanc, a Gran Meliá Hotel</td><td>Menorca</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>La Zambra Resort Mijas - Marbella The Unbound Collection By Hyatt</td><td>Mijas</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Finca Serena, Mallorca</td><td>Montuïri, Mallorca</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Nobis Hotel Palma</td><td>Palma de Mallorca</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Four Seasons Resort Mallorca at Formentor</td><td>Pollença</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Lodge Mallorca</td><td>Pollença</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Akelarre</td><td>San Sebastián</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Maria Cristina, a Luxury Collection Hotel</td><td>San Sebastián</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Nobu Hotel San Sebastián</td><td>San Sebastián</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>SLS Barcelona</td><td>Sant Adria de Besos</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hospes Las Casas del Rey de Baeza, a Member of Design Hotels</td><td>Seville</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Alfonso XIII, a Luxury Collection Hotel, Seville</td><td>Seville</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Hotel Colon, a Gran Melia Hotel</td><td>Seville</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Radisson Collection, Magdalena Plaza Sevilla</td><td>Seville</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Jumeirah Mallorca</td><td>Sóller</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>Fairmont La Hacienda Costa del Sol</td><td>Sotogrande</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>SO/ Sotogrande Spa and Golf Resort Hotel Costa del Sol</td><td>Sotogrande</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain" data-reviewed="0"><td>The Ritz-Carlton Tenerife, Abama</td><td>Tenerife</td><td>Spain</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden" data-reviewed="0"><td>At Six</td><td>Stockholm</td><td>Sweden</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden" data-reviewed="0"><td>Grand Hôtel Stockholm</td><td>Stockholm</td><td>Sweden</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden" data-reviewed="0"><td>Hotel Skeppsholmen, Stockholm, a Member of Design Hotels</td><td>Stockholm</td><td>Sweden</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden" data-reviewed="0"><td>Nobis Hotel Stockholm</td><td>Stockholm</td><td>Sweden</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Radisson Blu Hotel Reussen Andermatt</td><td>Andermatt</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Tschuggen Grand Hotel</td><td>Arosa</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Hotel Eden Roc</td><td>Ascona</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Crans Ambassador</td><td>Crans-Montana</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Six Senses Crans-Montana</td><td>Crans-Montana</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Kempinski Palace Engelberg</td><td>Engelberg</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Four Seasons Hotel des Bergues Geneva</td><td>Geneva</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Hotel D&#x27;Angleterre Geneva</td><td>Geneva</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>La Reserve Geneve - Hotel &amp; Spa</td><td>Geneva</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>The Ritz-Carlton Hotel de la Paix, Geneva</td><td>Geneva</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>The Alpina Gstaad</td><td>Gstaad</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>The View Lugano</td><td>Lugano</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Carlton Hotel St Moritz</td><td>St. Moritz</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Grand Hotel des Bains Kempinski</td><td>St. Moritz</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Alex Lake Zürich</td><td>Thalwil (Zurich)</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>W Verbier</td><td>Verbier</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Mont Cervin Palace</td><td>Zermatt</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>La Réserve Eden au Lac Zurich</td><td>Zürich</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Park Hyatt Zurich</td><td>Zürich</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>The Dolder Grand</td><td>Zürich</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland" data-reviewed="0"><td>Widder Hotel</td><td>Zürich</td><td>Switzerland</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Intercontinental Grand Ankara by IHG</td><td>Ankara</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Six Senses Kaplankaya</td><td>Bodrum</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Ariana Sustainable Luxury Lodge - Special Class</td><td>Cappadocia</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Aliée Istanbul - A Paris Society Collection Hotel</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Four Seasons Hotel Istanbul at Sultanahmet - Special Class</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Four Seasons Hotel Istanbul at the Bosphorus</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>Raffles Istanbul</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>The Bank Hotel Istanbul</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>The Peninsula Istanbul</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye" data-reviewed="0"><td>The Ritz-Carlton, Istanbul</td><td>Istanbul</td><td>Türkiye</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Coworth Park - Dorchester Collection</td><td>Ascot</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Royal Crescent Hotel &amp; Spa</td><td>Bath</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>100 Princes Street</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>InterContinental Edinburgh The George by IHG</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Kimpton Charlotte Square by IHG</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Balmoral Hotel</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Gleneagles Townhouse</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Virgin Hotels Edinburgh</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>W Edinburgh</td><td>Edinburgh</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Fairmont Windsor Park</td><td>Egham</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Glenapp Castle</td><td>Girvan</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Trump Turnberry</td><td>Girvan</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Kimpton Blythswood Square Hotel</td><td>Glasgow</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Gleneagles Hotel</td><td>Gleneagles</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Four Seasons Hotel Hampshire</td><td>Hampshire</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>1 Hotel Mayfair</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>11 Cadogan Gardens and The Apartments</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>45 Park Lane - Dorchester Collection</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Aethos London Shoreditch</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Brown&#x27;s Hotel, a Rocco Forte Hotel</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Bulgari Hotel London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Claridge&#x27;s</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>COMO Metropolitan London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Corinthia London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Dorset Square Hotel, Firmdale Hotels</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Four Seasons Hotel London at Park Lane</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Four Seasons Hotel London at Tower Bridge</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Grosvenor House Suites</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Haymarket Hotel, Firmdale Hotels</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Hotel Cafe Royal, London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>InterContinental London Park Lane by IHG</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Kimpton Fitzroy London by IHG</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>NoMad London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>One Aldwych</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Park Hyatt London River Thames</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Raffles London at The OWO</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="1"><td>Shangri-La The Shard, London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td><a href="https://www.youtube.com/watch?v=qTc6jlWKKzU">Video</a></td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Six Senses London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>St Martins Lane London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Berkeley, Maybourne</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Cadogan, A Belmond Hotel, London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Chelsea Townhouse</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Connaught</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Dorchester</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Emory</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Lanesborough, Oetker Hotels</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Langham, London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The London EDITION</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Londoner Hotel</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Marylebone Hotel</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Milestone Hotel &amp; Residences</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Ned</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Peninsula London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Savoy, A Fairmont Managed Hotel</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Soho Hotel, Firmdale Hotels</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Standard, London</td><td>London</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Cliveden House</td><td>Maidenhead</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Chewton Glen Hotel &amp; Spa</td><td>New Forest</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Estelle Manor</td><td>Oxford</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>Le Manoir aux Quat&#x27;Saisons</td><td>Oxford</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom" data-reviewed="0"><td>The Langley, a Luxury Collection Hotel, Buckinghamshire</td><td>Slough</td><td>United Kingdom</td><td>Europe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Botswana" data-reviewed="0"><td>Belmond Safaris</td><td>Okavango Delta</td><td>Botswana</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Botswana" data-reviewed="0"><td>Xigera Safari Lodge</td><td>Okavango Delta</td><td>Botswana</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt" data-reviewed="0"><td>Four Seasons Hotel Alexandria at San Stefano</td><td>Alexandria</td><td>Egypt</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt" data-reviewed="0"><td>Four Seasons Hotel Cairo at First Residence</td><td>Cairo</td><td>Egypt</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt" data-reviewed="0"><td>Four Seasons Hotel Cairo at Nile Plaza</td><td>Cairo</td><td>Egypt</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt" data-reviewed="0"><td>Four Seasons Resort Sharm EL Sheikh</td><td>Sharm El Sheikh</td><td>Egypt</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius" data-reviewed="0"><td>Four Seasons Mauritius at Anahita</td><td>Mauritius</td><td>Mauritius</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius" data-reviewed="0"><td>LUX* Grand Baie</td><td>Mauritius</td><td>Mauritius</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius" data-reviewed="0"><td>One&amp;Only Le Saint Géran</td><td>Mauritius</td><td>Mauritius</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Four Seasons Hotel Casablanca</td><td>Casablanca</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Four Seasons Resort Marrakech</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Kasbah Tamadot</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>La Sultana Marrakech</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Nobu Hotel Marrakech</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Park Hyatt Marrakech</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Royal Mansour Marrakech</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>The Oberoi Marrakech</td><td>Marrakech</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco" data-reviewed="0"><td>Four Seasons Hotel Rabat at Kasr Al Bahr</td><td>Rabat</td><td>Morocco</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Rwanda" data-reviewed="0"><td>Nyungwe Tea Forest Resort</td><td>Nyungwe</td><td>Rwanda</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Rwanda" data-reviewed="0"><td>One&amp;Only Nyungwe House</td><td>Nyungwe</td><td>Rwanda</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles" data-reviewed="0"><td>Four Seasons Resort Seychelles</td><td>Seychelles</td><td>Seychelles</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles" data-reviewed="0"><td>Four Seasons Resort Seychelles at Desroches Island</td><td>Seychelles</td><td>Seychelles</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles" data-reviewed="0"><td>Six Senses Zil Pasyon Seychelles</td><td>Seychelles</td><td>Seychelles</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa" data-reviewed="0"><td>Cape Grace, A Fairmont Managed Hotel</td><td>Cape Town</td><td>South Africa</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa" data-reviewed="0"><td>Ellerman House</td><td>Cape Town</td><td>South Africa</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa" data-reviewed="0"><td>Mount Nelson, A Belmond Hotel, Cape Town</td><td>Cape Town</td><td>South Africa</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa" data-reviewed="0"><td>One&amp;Only Cape Town</td><td>Cape Town</td><td>South Africa</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa" data-reviewed="0"><td>The Twelve Apostles Hotel and Spa</td><td>Cape Town</td><td>South Africa</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa" data-reviewed="0"><td>Four Seasons Hotel The Westcliff, Johannesburg</td><td>Johannesburg</td><td>South Africa</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Tunisia" data-reviewed="0"><td>Four Seasons Hotel Tunis</td><td>Tunis</td><td>Tunisia</td><td>Africa</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Azerbaijan" data-reviewed="0"><td>Four Seasons Hotel Baku</td><td>Baku</td><td>Azerbaijan</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Bahrain" data-reviewed="0"><td>Four Seasons Hotel Bahrain Bay</td><td>Manama</td><td>Bahrain</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel" data-reviewed="0"><td>King David, Jerusalem</td><td>Jerusalem</td><td>Israel</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel" data-reviewed="0"><td>Mamilla Hotel</td><td>Jerusalem</td><td>Israel</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel" data-reviewed="0"><td>The David Citadel Jerusalem</td><td>Jerusalem</td><td>Israel</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel" data-reviewed="0"><td>InterContinental David Tel Aviv by IHG</td><td>Tel Aviv</td><td>Israel</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Jordan" data-reviewed="0"><td>Four Seasons Hotel Amman</td><td>Amman</td><td>Jordan</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Kuwait" data-reviewed="0"><td>Four Seasons Hotel Kuwait at Burj Alshaya</td><td>Kuwait City</td><td>Kuwait</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Qatar" data-reviewed="0"><td>Four Seasons Hotel Doha</td><td>Doha</td><td>Qatar</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Qatar" data-reviewed="0"><td>Four Seasons Resort And Residences At The Pearl - Qatar</td><td>Doha</td><td>Qatar</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia" data-reviewed="0"><td>Six Senses Southern Dunes, The Red Sea</td><td>Red Sea</td><td>Saudi Arabia</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia" data-reviewed="0"><td>The St. Regis Red Sea Resort</td><td>Red Sea</td><td>Saudi Arabia</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia" data-reviewed="0"><td>Four Seasons Hotel Riyadh</td><td>Riyadh</td><td>Saudi Arabia</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia" data-reviewed="0"><td>Kimpton KAFD Riyadh by IHG</td><td>Riyadh</td><td>Saudi Arabia</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Four Seasons Hotel Abu Dhabi at Al Maryah Island</td><td>Abu Dhabi</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Atlantis The Royal</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Bulgari Resort Dubai</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Four Seasons Hotel Dubai International Financial Centre</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Four Seasons Resort Dubai at Jumeirah Beach</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>InterContinental Residences Dubai Business Bay by IHG</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Jumeirah Al Naseem Dubai</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Jumeirah Burj Al Arab Dubai</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Jumeirah Dar Al Masyaf</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Jumeirah Marsa Al Arab</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>One&amp;Only The Palm</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>SLS Dubai Hotel &amp; Residences</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>SO/ Uptown Dubai</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>Taj Dubai</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>The Lana - Dorchester Collection</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates" data-reviewed="0"><td>The Ritz-Carlton, Dubai</td><td>Dubai</td><td>United Arab Emirates</td><td>Middle East</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia" data-reviewed="0"><td>Six Senses Krabey Island</td><td>Krabey Island</td><td>Cambodia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia" data-reviewed="0"><td>Raffles Grand Hotel d&#x27;Angkor</td><td>Siem Reap</td><td>Cambodia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia" data-reviewed="0"><td>Shinta Mani Angkor</td><td>Siem Reap</td><td>Cambodia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Bulgari Hotel Beijing</td><td>Beijing</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Four Seasons Hotel Beijing</td><td>Beijing</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>The Peninsula Beijing</td><td>Beijing</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Four Seasons Hotel Hangzhou At Hangzhou Centre</td><td>Hangzhou</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Four Seasons Hotel Hangzhou at West Lake</td><td>Hangzhou</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Rissai Valley, a Ritz-Carlton Reserve</td><td>Jiuzhaigou</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Bulgari Hotel Shanghai</td><td>Shanghai</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Kimpton Qiantan Shanghai by IHG</td><td>Shanghai</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>The Peninsula Shanghai</td><td>Shanghai</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>The Shanghai EDITION</td><td>Shanghai</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Upper House Shanghai</td><td>Shanghai</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Four Seasons Hotel Shenzhen</td><td>Shenzhen</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>The Langham, Shenzhen</td><td>Shenzhen</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Four Seasons Hotel Suzhou</td><td>Suzhou</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Four Seasons Hotel Tianjin</td><td>Tianjin</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China" data-reviewed="0"><td>Intercontinental Zhengzhou by IHG</td><td>Zhengzhou</td><td>China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>Four Seasons Hotel Hong Kong</td><td>Hong Kong</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>Island Shangri-La, Hong Kong</td><td>Hong Kong</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>Mondrian Hong Kong</td><td>Hong Kong</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>The Langham, Hong Kong</td><td>Hong Kong</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>Upper House Hong Kong</td><td>Hong Kong</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>Kerry Hotel, Hong Kong</td><td>Kowloon</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>Regent Hong Kong</td><td>Kowloon</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China" data-reviewed="0"><td>The Peninsula Hong Kong</td><td>Kowloon</td><td>Hong Kong SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Four Seasons Hotel Bengaluru at Embassy One</td><td>Bengaluru</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Six Senses Vana - A Wellness Retreat</td><td>Dehradun</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Raffles Jaipur</td><td>Jaipur</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>The Oberoi Rajvilas</td><td>Jaipur</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Four Seasons Hotel Mumbai</td><td>Mumbai</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>The Taj Mahal Palace Mumbai</td><td>Mumbai</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Taj Mahal, New Delhi</td><td>New Delhi</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>The Leela Palace New Delhi</td><td>New Delhi</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>The Oberoi, New Delhi</td><td>New Delhi</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Six Senses Fort Barwara</td><td>Ranthambore</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>Raffles Udaipur</td><td>Udaipur</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India" data-reviewed="0"><td>The Oberoi Udaivilas</td><td>Udaipur</td><td>India</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Andaz Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Bvlgari Resort Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>COMO Canggu</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>COMO Shambhala Estate</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>COMO Uma Canggu</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Four Seasons Resort Bali at Jimbaran Bay</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Four Seasons Resort Bali at Sayan</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Jimbaran Puri, A Belmond Hotel, Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Jumeirah Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Mandapa, a Ritz-Carlton Reserve</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Raffles Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Regent Bali Canggu</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Six Senses Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Soori Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>The Apurva Kempinski Bali</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>The St. Regis Bali Resort</td><td>Bali</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>Four Seasons Hotel Jakarta</td><td>Jakarta</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>The Langham, Jakarta</td><td>Jakarta</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia" data-reviewed="0"><td>NIHI Sumba</td><td>Sumba</td><td>Indonesia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Ace Hotel Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Banyan Tree Higashiyama Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Four Seasons Hotel Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Garrya Nijo Castle Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Park Hyatt Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Six Senses Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Sowaka</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="1"><td>Suiran, A Luxury Collection Hotel, Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td><a href="https://visitkarma.com/p/suiran-kyoto-arashiyama-review-marriott-luxury-collection-onsen-ryokan-stay/">Blog</a> · <a href="https://www.youtube.com/watch?v=RJSN7wgPO40">Video</a></td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Ritz-Carlton, Kyoto</td><td>Kyoto</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>IRAPH SUI, a Luxury Collection Hotel, Miyako Okinawa</td><td>Miyakojima</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Ritz-Carlton, Nikko</td><td>Nikko</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Park Hyatt Niseko Hanazono</td><td>Niseko</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Four Seasons Hotel Osaka</td><td>Osaka</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>InterContinental Osaka by IHG</td><td>Osaka</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Ritz-Carlton, Osaka</td><td>Osaka</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>W Osaka</td><td>Osaka</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Andaz Tokyo Toranomon Hills</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Bellustar Tokyo, a Pan Pacific Hotel</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Bulgari Hotel Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Fairmont Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Four Seasons Hotel Tokyo at Marunouchi</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Four Seasons Hotel Tokyo at Otemachi</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Grand Hyatt Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Kimpton Shinjuku Tokyo by IHG</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Palace Hotel Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>Park Hyatt Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="1"><td>Shangri-La Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td><a href="https://visitkarma.com/p/shangri-la-tokyo-review/">Blog</a> · <a href="https://www.youtube.com/watch?v=0-9yoNhmLtk">Video</a></td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Okura Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Peninsula Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Prince Gallery Tokyo Kioicho, a Luxury Collection Hotel</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Ritz-Carlton, Tokyo</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Strings by InterContinental Tokyo by IHG</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Tokyo EDITION, Ginza</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan" data-reviewed="0"><td>The Tokyo EDITION, Toranomon</td><td>Tokyo</td><td>Japan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Macao SAR China" data-reviewed="0"><td>Four Seasons Hotel Macao</td><td>Macau</td><td>Macao SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Macao SAR China" data-reviewed="0"><td>The Grand Suites at Four Seasons</td><td>Macau</td><td>Macao SAR China</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia" data-reviewed="0"><td>Four Seasons Hotel Kuala Lumpur</td><td>Kuala Lumpur</td><td>Malaysia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia" data-reviewed="0"><td>Four Seasons Resort Langkawi</td><td>Langkawi</td><td>Malaysia</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>COMO Cocoa Island</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Four Seasons Maldives At Kuda Huraa</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Four Seasons Maldives at Landaa Giraavaru</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>InterContinental Maldives Maamunagau Resort by IHG</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>JOALI Maldives</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>LUX* South Ari Atoll</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Naladhu Private Island Maldives Resort</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>One&amp;Only Reethi Rah</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Six Senses Kanuhura</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Six Senses Laamu</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Soneva Fushi</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives" data-reviewed="0"><td>Taj Exotica Resort &amp; Spa, Maldives</td><td>Maldives</td><td>Maldives</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines" data-reviewed="0"><td>Shangri-La Boracay</td><td>Boracay</td><td>Philippines</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines" data-reviewed="0"><td>Raffles Makati</td><td>Manila</td><td>Philippines</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines" data-reviewed="0"><td>Shangri-La The Fort, Manila</td><td>Manila</td><td>Philippines</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines" data-reviewed="0"><td>The Peninsula Manila</td><td>Manila</td><td>Philippines</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Capella Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>COMO Metropolitan Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Four Seasons Hotel Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>InterContinental Singapore Robertson Quay by IHG</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>JW Marriott Hotel Singapore South Beach</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Marina Bay Sands</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Mondrian Singapore Duxton</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Pan Pacific Orchard</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Pan Pacific Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>Raffles Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>The Fullerton Bay Hotel Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>The Ritz-Carlton, Millenia Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>The St. Regis Singapore (Newly Renovated)</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore" data-reviewed="0"><td>The Standard, Singapore</td><td>Singapore</td><td>Singapore</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea" data-reviewed="0"><td>Four Seasons Hotel Seoul</td><td>Seoul</td><td>South Korea</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea" data-reviewed="0"><td>InterContinental Grand Seoul Parnas</td><td>Seoul</td><td>South Korea</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea" data-reviewed="0"><td>Mondrian Seoul Itaewon</td><td>Seoul</td><td>South Korea</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea" data-reviewed="0"><td>Park Hyatt Seoul</td><td>Seoul</td><td>South Korea</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea" data-reviewed="0"><td>The Shilla Seoul</td><td>Seoul</td><td>South Korea</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan" data-reviewed="0"><td>Hotel Proverbs Taipei</td><td>Taipei</td><td>Taiwan</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Andaz One Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Capella Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Four Seasons Hotel Bangkok at Chao Phraya River</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Kimpton Maa-Lai Bangkok by IHG</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Park Hyatt Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Sindhorn Kempinski Hotel Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The Peninsula Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The Ritz-Carlton, Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The Siam</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The St. Regis Bangkok</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The Standard, Bangkok Mahanakhon</td><td>Bangkok</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Anantara Chiang Mai Resort</td><td>Chiang Mai</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Four Seasons Resort Chiang Mai</td><td>Chiang Mai</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Four Seasons Tented Camp Golden Triangle</td><td>Golden Triangle</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Devasom Khao Lak Beach Resort &amp; Villas</td><td>Khao Lak</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Anantara Lawana Koh Samui Resort</td><td>Koh Samui</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Banyan Tree Samui</td><td>Koh Samui</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Four Seasons Resort Koh Samui</td><td>Koh Samui</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Kimpton Kitalay Samui by IHG</td><td>Koh Samui</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The Ritz-Carlton, Koh Samui</td><td>Koh Samui</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Vana Belle, a Luxury Collection Resort, Koh Samui</td><td>Koh Samui</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Banyan Tree Krabi</td><td>Krabi</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Phulay Bay, a Ritz-Carlton Reserve</td><td>Krabi</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Andaz Pattaya Jomtien Beach</td><td>Pattaya</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>InterContinental Pattaya Resort by IHG</td><td>Pattaya</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Anantara Layan Phuket Resort &amp; Layan Residences</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Banyan Tree Phuket</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Dinso Resort &amp; Villas Phuket, Vignette Collection by IHG</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Iniala Beach House</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>InterContinental Phuket Resort by IHG</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Keemala</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>The Naka Island, a Luxury Collection Resort &amp; Spa, Phuket</td><td>Phuket</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand" data-reviewed="0"><td>Anantara Rasananda Koh Phangan Villas</td><td>Suratthani</td><td>Thailand</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Six Senses Con Dao</td><td>Con Dao</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>InterContinental Halong Bay Resort by IHG</td><td>Ha Long Bay</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Capella Hanoi</td><td>Hanoi</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Sofitel Legend Metropole Hanoi</td><td>Hanoi</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Four Seasons Resort The Nam Hai, Hoi An, Vietnam</td><td>Hoi An</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Moire Hoi An, Vignette Collection</td><td>Hoi An</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Banyan Tree Lang Co</td><td>Lang Co</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Six Senses Ninh Van Bay</td><td>Ninh Van Bay</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>JW Marriott Phu Quoc Emerald Bay Resort &amp; Spa</td><td>Phu Quoc</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam" data-reviewed="0"><td>Regent Phu Quoc</td><td>Phu Quoc</td><td>Vietnam</td><td>Asia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Mount Lofty House &amp; Estate Adelaide Hills - Adults Retreat</td><td>Adelaide Hills</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>W Brisbane</td><td>Brisbane</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Shangri-La The Marina, Cairns</td><td>Cairns</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>1 Hotel Melbourne</td><td>Docklands</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>The Langham, Gold Coast</td><td>Gold Coast</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Park Hyatt Melbourne</td><td>Melbourne</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Sofitel Melbourne On Collins</td><td>Melbourne</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>The Langham, Melbourne</td><td>Melbourne</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>W Melbourne</td><td>Melbourne</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>COMO The Treasury</td><td>Perth</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>The Ritz-Carlton, Perth</td><td>Perth</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Four Seasons Hotel Sydney</td><td>Sydney</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>InterContinental Sydney by IHG</td><td>Sydney</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Kimpton Margot Sydney by IHG</td><td>Sydney</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>Shangri-La Sydney</td><td>Sydney</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia" data-reviewed="0"><td>The Langham, Sydney</td><td>Sydney</td><td>Australia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji" data-reviewed="0"><td>Nanuku Resort, Fiji</td><td>Fiji</td><td>Fiji</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji" data-reviewed="0"><td>Six Senses Fiji</td><td>Fiji</td><td>Fiji</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji" data-reviewed="0"><td>Sofitel Fiji Resort &amp; Spa Denarau Island</td><td>Fiji</td><td>Fiji</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>Four Seasons Resort Bora Bora</td><td>Bora Bora</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>InterContinental Bora Bora Resort and Thalasso Spa by IHG</td><td>Bora Bora</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>Le Bora Bora</td><td>Bora Bora</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>The St. Regis Bora Bora Resort</td><td>Bora Bora</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>The Westin Bora Bora Resort &amp; Spa</td><td>Bora Bora</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>Sofitel Kia Ora Moorea Beach Resort</td><td>Moorea</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>Le Taha&#x27;a</td><td>Tapuamu</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia" data-reviewed="0"><td>The Brando</td><td>Tetiaroa</td><td>French Polynesia</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand" data-reviewed="0"><td>Cordis, Auckland</td><td>Auckland</td><td>New Zealand</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand" data-reviewed="0"><td>Hotel Indigo Auckland by IHG</td><td>Auckland</td><td>New Zealand</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand" data-reviewed="0"><td>InterContinental Auckland</td><td>Auckland</td><td>New Zealand</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand" data-reviewed="0"><td>Park Hyatt Auckland</td><td>Auckland</td><td>New Zealand</td><td>Oceania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand" data-reviewed="0"><td>Blanket Bay</td><td>Glenorchy</td><td>New Zealand</td><td>Oceania</td><td>—</td></tr>
</tbody></table>

