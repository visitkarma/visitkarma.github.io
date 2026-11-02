---
title: "The Edit by Chase Travel: Every Hotel, by Region and Country"
date: 2026-11-02
lastmod: 2026-11-02
slug: "chase-the-edit-hotel-list"
description: "The full list of The Edit by Chase Travel hotels — 1,528 properties in 92 countries, grouped by region, country and city, searchable and filterable — plus how the Sapphire Reserve hotel credits and perks work."
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

Use the search box to find a hotel, city, or country, or pick a region or country from the menus — the tables filter live, and the count below the menus tells you how many hotels match. Where we have reviewed a hotel ourselves, the **Our review** column links to our blog post and YouTube video for it. (Our MGM Grand video is a warning, not a recommendation — it is linked because it is our honest take on that hotel, same as the rest.)

## The list below

This is every Edit hotel in Chase Travel's list as compiled on November 2, 2026: **1,528 hotels in 92 countries**, grouped by region, then country, then state or city. One near-duplicate pair from the source is kept as listed (two similar Nekajui Peninsula Papagayo entries in Costa Rica), so the unique-property count may be 1,527.

Hotel membership changes through the year — hotels join and leave — so confirm a hotel is still in The Edit in Chase Travel before you plan around it. This page is a reference list, not a booking site, and we are not paid by Chase or any hotel on it. The list itself comes from a third-party compilation of Chase Travel's list, not from Chase directly: Chase publishes no complete public list of its own.

<div class="hotel-filter">
<p><label>Search hotels, cities or countries: <input type="search" id="hotel-search" placeholder="e.g. Kyoto, Four Seasons, Italy"></label></p>
<p><label>Region: <select id="hotel-region"><option value="">All regions</option></select></label>
<label>Country: <select id="hotel-country"><option value="">All countries</option></select></label>
<button type="button" id="hotel-reset">Clear filters</button></p>
<p id="hotel-count" aria-live="polite"></p>
<p><small>Tip: the country menu also works as a jump menu — pick a country to see only its hotels. With JavaScript off, the full lists below still show; only the filtering needs JavaScript.</small></p>
</div>
<script>
(function () {
  var search = document.getElementById('hotel-search');
  var regionSel = document.getElementById('hotel-region');
  var countrySel = document.getElementById('hotel-country');
  var countEl = document.getElementById('hotel-count');
  var rows = Array.prototype.slice.call(document.querySelectorAll('tr.hotel-row'));
  var total = rows.length;
  var regions = [], countries = [];
  rows.forEach(function (r) {
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
      var ok = (!q || r.textContent.toLowerCase().indexOf(q) !== -1)
        && (!reg || r.dataset.region === reg)
        && (!ctry || r.dataset.country === ctry);
      r.style.display = ok ? '' : 'none';
      if (ok) shown++;
    });
    // Hide country (h3) and state (h4) headings + their tables when no rows show.
    ['h3', 'h4'].forEach(function (tag) {
      Array.prototype.slice.call(document.querySelectorAll(tag)).forEach(function (h) {
        var el = h.nextElementSibling, any = false;
        while (el && el.tagName !== 'H2' && el.tagName !== 'H3' && el.tagName !== 'H4') {
          if (el.tagName === 'TABLE') {
            any = Array.prototype.slice.call(el.querySelectorAll('tr.hotel-row')).some(function (r) { return r.style.display !== 'none'; });
          }
          el = el.nextElementSibling;
        }
        h.style.display = any ? '' : 'none';
        var t = h.nextElementSibling;
        while (t && t.tagName !== 'H2' && t.tagName !== 'H3' && t.tagName !== 'H4') {
          if (t.tagName === 'TABLE') t.style.display = any ? '' : 'none';
          t = t.nextElementSibling;
        }
      });
    });
    // Hide region (h2) headings when all their countries are hidden.
    Array.prototype.slice.call(document.querySelectorAll('h2')).forEach(function (h) {
      var el = h.nextElementSibling, any = false;
      while (el && el.tagName !== 'H2') {
        if ((el.tagName === 'H3' || el.tagName === 'H4') && el.style.display !== 'none') any = true;
        el = el.nextElementSibling;
      }
      h.style.display = any ? '' : 'none';
    });
    countEl.textContent = 'Showing ' + shown + ' of ' + total + ' hotels.';
  }
  document.getElementById('hotel-reset').addEventListener('click', function () {
    search.value = ''; regionSel.value = ''; countrySel.value = ''; apply();
  });
  search.addEventListener('input', apply);
  regionSel.addEventListener('change', apply);
  countrySel.addEventListener('change', apply);
  apply();
})();
</script>

## North America

### Canada

#### Banff

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Banff Springs</td><td>Banff</td><td>—</td></tr>
</tbody></table>

#### Fogo Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fogo Island Inn</td><td>Fogo Island</td><td>—</td></tr>
</tbody></table>

#### Halifax

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Muir, a Luxury Collection Hotel, Halifax</td><td>Halifax</td><td>—</td></tr>
</tbody></table>

#### Jasper

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Jasper Park Lodge</td><td>Jasper</td><td>—</td></tr>
</tbody></table>

#### Lake Louise

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Chateau Lake Louise</td><td>Lake Louise</td><td>—</td></tr>
</tbody></table>

#### Montreal

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont The Queen Elizabeth</td><td>Montreal</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Four Seasons Hotel Montreal</td><td>Montreal</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Sofitel Montreal Golden Mile</td><td>Montreal</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Ritz-Carlton, Montreal</td><td>Montreal</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Vogue Hotel Montreal Downtown, Curio Collection by Hilton</td><td>Montreal</td><td>—</td></tr>
</tbody></table>

#### Ottawa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Chateau Laurier</td><td>Ottawa</td><td>—</td></tr>
</tbody></table>

#### Québec City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Auberge Saint-Antoine</td><td>Québec City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Le Chateau Frontenac</td><td>Québec City</td><td>—</td></tr>
</tbody></table>

#### Toronto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>1 Hotel Toronto</td><td>Toronto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Four Seasons Hotel Toronto</td><td>Toronto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Park Hyatt Toronto</td><td>Toronto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Shangri-La, Toronto</td><td>Toronto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Ritz-Carlton, Toronto</td><td>Toronto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The St. Regis Toronto</td><td>Toronto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>W Toronto</td><td>Toronto</td><td>—</td></tr>
</tbody></table>

#### Vancouver

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Hotel Vancouver</td><td>Vancouver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Pacific Rim</td><td>Vancouver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Waterfront</td><td>Vancouver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Hyatt Vancouver Alberni Downtown</td><td>Vancouver</td><td>—</td></tr>
</tbody></table>

#### Victoria

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Empress</td><td>Victoria</td><td>—</td></tr>
</tbody></table>

#### Whistler

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Chateau Whistler</td><td>Whistler</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Four Seasons Resort Whistler</td><td>Whistler</td><td>—</td></tr>
</tbody></table>

### Mexico

#### Akumal

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Secrets Akumal Riviera Maya</td><td>Akumal</td><td>—</td></tr>
</tbody></table>

#### Cabo San Lucas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Corazon Cabo Resort &amp; Spa</td><td>Cabo San Lucas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Los Cabos - All Inclusive</td><td>Cabo San Lucas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>ME Cabo by Meliá – Adults Only – SLH</td><td>Cabo San Lucas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Montage Los Cabos</td><td>Cabo San Lucas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Nobu Hotel Los Cabos</td><td>Cabo San Lucas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Park Hyatt Cabo Del Sol</td><td>Cabo San Lucas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Cape, a Thompson Hotel</td><td>Cabo San Lucas</td><td>—</td></tr>
</tbody></table>

#### Cancun

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Impression Isla Mujeres by Secrets</td><td>Cancun</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kempinski Hotel Cancún</td><td>Cancun</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>NIZUC Resort &amp; Spa</td><td>Cancun</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>SLS Cancun</td><td>Cancun</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>SLS Playa Mujeres – ALL Inclusive Collection</td><td>Cancun</td><td>—</td></tr>
</tbody></table>

#### Costalegre

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Resort Tamarindo</td><td>Costalegre</td><td>—</td></tr>
</tbody></table>

#### Cozumel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>InterContinental Presidente Cozumel Resort &amp; Spa</td><td>Cozumel</td><td>—</td></tr>
</tbody></table>

#### Guadalajara

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Casa Habita, Guadalajara, a Member of Design Hotels</td><td>Guadalajara</td><td>—</td></tr>
</tbody></table>

#### Kantenah

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Unico Hotel Riviera Maya - Adults Only</td><td>Kantenah</td><td>—</td></tr>
</tbody></table>

#### La Ribera

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Resort Los Cabos at Costa Palmas</td><td>La Ribera</td><td>—</td></tr>
</tbody></table>

#### Lo de Marcos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>One&amp;Only Mandarina</td><td>Lo de Marcos</td><td>—</td></tr>
</tbody></table>

#### Mérida

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Chable Yucatan</td><td>Mérida</td><td>—</td></tr>
</tbody></table>

#### Mexico City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Andaz Condesa Mexico City</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Circulo Mexicano, Mexico, a Member of Design Hotels</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Condesa df, Mexico City, a Member of Design Hotels</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Hotel Mexico City</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Alexander</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kimpton Virgilio Hotel</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Mondrian Mexico City Condesa</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Sofitel Mexico City Reforma</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Ritz-Carlton Residences Mexico City</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Ritz-Carlton, Mexico City</td><td>Mexico City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St. Regis Mexico City</td><td>Mexico City</td><td>—</td></tr>
</tbody></table>

#### Monterrey

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>InterContinental Presidente Monterrey by IHG</td><td>Monterrey</td><td>—</td></tr>
</tbody></table>

#### Nuevo Nayarit

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Riviera Nayarit - All Inclusive</td><td>Nuevo Nayarit</td><td>—</td></tr>
</tbody></table>

#### Oaxaca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Otro Oaxaca</td><td>Oaxaca</td><td>—</td></tr>
</tbody></table>

#### Playa del Carmen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Alila Mayakoba</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Mayakoba</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Chablé Maroma</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Fairmont Heritage Place, Mayakoba</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Riviera Maya - All Inclusive</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Esencia</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Impression Moxche by Secrets</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>La Casa de la Playa</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Maroma, A Belmond Hotel, Riviera Maya</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Palmaïa-The House of AïA: All Inclusive Wellness Resort</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Paradisus La Perla</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Paradisus Playa del Carmen</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Riviera Maya EDITION at Kanai</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St. Regis Kanai Resort, Riviera Maya</td><td>Playa del Carmen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Viceroy Riviera Maya, a Luxury Villa Resort - Adults Only</td><td>Playa del Carmen</td><td>—</td></tr>
</tbody></table>

#### Puebla

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Puebla</td><td>Puebla</td><td>—</td></tr>
</tbody></table>

#### Puerto Vallarta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Casa Velas Adults Only All Inclusive</td><td>Puerto Vallarta</td><td>—</td></tr>
</tbody></table>

#### Punta de Mita

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Resort Punta Mita</td><td>Punta de Mita</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Naviva, A Four Seasons Resort, Punta Mita, Mexico - All Inclusive</td><td>Punta de Mita</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St. Regis Punta Mita Resort</td><td>Punta de Mita</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>W Punta de Mita</td><td>Punta de Mita</td><td>—</td></tr>
</tbody></table>

#### San José del Cabo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Boutique Los Cabos</td><td>San José del Cabo</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>One&amp;Only Palmilla, Los Cabos</td><td>San José del Cabo</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Residences at Zadún, a Ritz-Carlton Reserve</td><td>San José del Cabo</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Solaz, A Luxury Collection Resort, Los Cabos a Marriott Hotel</td><td>San José del Cabo</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Viceroy Los Cabos</td><td>San José del Cabo</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Zadún, a Ritz-Carlton Reserve</td><td>San José del Cabo</td><td>—</td></tr>
</tbody></table>

#### San Miguel de Allende

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Casa de Sierra Nevada, A Belmond Hotel, San Miguel de Allende</td><td>San Miguel de Allende</td><td>—</td></tr>
</tbody></table>

#### Todos Santos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel San Cristobal</td><td>Todos Santos</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kimpton Mas Olas Resort and Spa</td><td>Todos Santos</td><td>—</td></tr>
</tbody></table>

#### Tulum

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>BE Destination Tulum</td><td>Tulum</td><td>—</td></tr>
</tbody></table>

#### Valle de Guadalupe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Veya Valle De Guadalupe</td><td>Valle de Guadalupe</td><td>—</td></tr>
</tbody></table>

#### Zihuatanejo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Thompson Zihuatanejo</td><td>Zihuatanejo</td><td>—</td></tr>
</tbody></table>

### United States

#### Auburn

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Laurel Hotel and Spa</td><td>Auburn</td><td>—</td></tr>
</tbody></table>

#### Morristown

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Castle Hot Springs</td><td>Morristown</td><td>—</td></tr>
</tbody></table>

#### Paradise Valley

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mountain Shadows Resort Scottsdale</td><td>Paradise Valley</td><td>—</td></tr>
</tbody></table>

#### Phoenix

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Phoenix Desert Ridge Resort &amp; Spa</td><td>Phoenix</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Royal Palms Resort &amp; Spa</td><td>Phoenix</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Global Ambassador</td><td>Phoenix</td><td>—</td></tr>
</tbody></table>

#### Scottsdale

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Scottsdale Resort &amp; Bungalows</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Caesars Republic Scottsdale, A Hilton Hotel</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Scottsdale Princess</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Scottsdale at Troon North</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Scottsdale Resort</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Scottsdale Camelback Inn Resort &amp; Spa</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Scottsdale Resort &amp; Spa at Montelucia</td><td>Scottsdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Phoenician, a Luxury Collection Resort, Scottsdale</td><td>Scottsdale</td><td>—</td></tr>
</tbody></table>

#### Sedona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amara Resort and Spa</td><td>Sedona</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ambiente A Landscape Hotel, Sedona</td><td>Sedona</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Enchantment Resort</td><td>Sedona</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Auberge de Sedona</td><td>Sedona</td><td>—</td></tr>
</tbody></table>

#### Tempe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Tempe Hotel at ASU</td><td>Tempe</td><td>—</td></tr>
</tbody></table>

#### Tucson

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canyon Ranch Tucson</td><td>Tucson</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Tucson National Resort</td><td>Tucson</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Dove Mountain</td><td>Tucson</td><td>—</td></tr>
</tbody></table>

#### Anaheim

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Anaheim Resort</td><td>Anaheim</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Anaheim Resort</td><td>Anaheim</td><td>—</td></tr>
</tbody></table>

#### Beverly Hills

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Beverly Wilshire, Beverly Hills, A Four Seasons Hotel</td><td>Beverly Hills</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Ermitage Beverly Hills</td><td>Beverly Hills</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Beverly Hills Hotel</td><td>Beverly Hills</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Maybourne Beverly Hills, Maybourne</td><td>Beverly Hills</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Peninsula Beverly Hills</td><td>Beverly Hills</td><td>—</td></tr>
</tbody></table>

#### Big Sur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alila Ventana Big Sur</td><td>Big Sur</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Post Ranch Inn</td><td>Big Sur</td><td>—</td></tr>
</tbody></table>

#### Calistoga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort and Residences Napa Valley</td><td>Calistoga</td><td>—</td></tr>
</tbody></table>

#### Carlsbad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Aviara Resort, Golf Club &amp; Spa</td><td>Carlsbad</td><td>—</td></tr>
</tbody></table>

#### Carmel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carmel Valley Ranch</td><td>Carmel</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Le Petit Pali at 8th Ave</td><td>Carmel</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Le Petit Pali at Ocean Ave</td><td>Carmel</td><td>—</td></tr>
</tbody></table>

#### Carmel Valley

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bernardus Lodge &amp; Spa</td><td>Carmel Valley</td><td>—</td></tr>
</tbody></table>

#### Dana Point

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Laguna Niguel</td><td>Dana Point</td><td>—</td></tr>
</tbody></table>

#### Del Mar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Auberge Del Mar</td><td>Del Mar</td><td>—</td></tr>
</tbody></table>

#### Encinitas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alila Marea Beach Resort Encinitas, a Hyatt Luxury Resort</td><td>Encinitas</td><td>—</td></tr>
</tbody></table>

#### Forestville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Farmhouse Inn</td><td>Forestville</td><td>—</td></tr>
</tbody></table>

#### Guerneville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dawn Ranch</td><td>Guerneville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Stavrand Russian River Valley</td><td>Guerneville</td><td>—</td></tr>
</tbody></table>

#### Half Moon Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Half Moon Bay</td><td>Half Moon Bay</td><td>—</td></tr>
</tbody></table>

#### Healdsburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Healdsburg</td><td>Healdsburg</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Liora Estate</td><td>Healdsburg</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Healdsburg</td><td>Healdsburg</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Madrona</td><td>Healdsburg</td><td>—</td></tr>
</tbody></table>

#### Huntington Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Huntington Beach Resort and Spa</td><td>Huntington Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Paséa Hotel &amp; Spa</td><td>Huntington Beach</td><td>—</td></tr>
</tbody></table>

#### Indian Wells

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Indian Wells Resort &amp; Villas</td><td>Indian Wells</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Tommy Bahama Miramonte Resort &amp; Spa</td><td>Indian Wells</td><td>—</td></tr>
</tbody></table>

#### Laguna Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Laguna Beach</td><td>Laguna Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch at Laguna Beach</td><td>Laguna Beach</td><td>—</td></tr>
</tbody></table>

#### Lake Tahoe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Lake Tahoe</td><td>Lake Tahoe</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Edgewood Tahoe Resort</td><td>Lake Tahoe</td><td>—</td></tr>
</tbody></table>

#### Los Angeles

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Downtown L.A. Proper</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Los Angeles at Beverly Hills</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bel-Air - Dorchester Collection</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Per La, Autograph Collection</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Los Angeles Downtown by IHG</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SLS Hotel, a Luxury Collection Hotel, Beverly Hills</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Los Angeles</td><td>Los Angeles</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Hollywood</td><td>Los Angeles</td><td>—</td></tr>
</tbody></table>

#### Malibu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Malibu Beach Inn</td><td>Malibu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch Malibu</td><td>Malibu</td><td>—</td></tr>
</tbody></table>

#### Mammoth Lakes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Mammoth</td><td>Mammoth Lakes</td><td>—</td></tr>
</tbody></table>

#### Menlo Park

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Nia, Autograph Collection</td><td>Menlo Park</td><td>—</td></tr>
</tbody></table>

#### Napa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carneros Resort and Spa</td><td>Napa</td><td>—</td></tr>
</tbody></table>

#### Newport Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lido House, Autograph Collection</td><td>Newport Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Newport Beach</td><td>Newport Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Resort at Pelican Hill</td><td>Newport Beach</td><td>—</td></tr>
</tbody></table>

#### Oceanside

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mission Pacific Beach Resort</td><td>Oceanside</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Seabird Resort</td><td>Oceanside</td><td>—</td></tr>
</tbody></table>

#### Ojai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ojai Valley Inn</td><td>Ojai</td><td>—</td></tr>
</tbody></table>

#### Palm Springs

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Avalon Hotel &amp; Bungalows Palm Springs, a Member of Design Hotels</td><td>Palm Springs</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ingleside Estate Hotel &amp; Bungalows- Adults Only</td><td>Palm Springs</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Parker Palm Springs</td><td>Palm Springs</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Palm Springs</td><td>Palm Springs</td><td>—</td></tr>
</tbody></table>

#### Palo Alto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Silicon Valley at East Palo Alto</td><td>Palo Alto</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Palo Alto</td><td>Palo Alto</td><td>—</td></tr>
</tbody></table>

#### Pasadena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham Huntington, Pasadena</td><td>Pasadena</td><td>—</td></tr>
</tbody></table>

#### Rancho Mirage

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Rancho Mirage</td><td>Rancho Mirage</td><td>—</td></tr>
</tbody></table>

#### Rancho Palos Verdes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Terranea Resort</td><td>Rancho Palos Verdes</td><td>—</td></tr>
</tbody></table>

#### Rancho Santa Fe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn At Rancho Santa Fe</td><td>Rancho Santa Fe</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rancho Valencia Resort and Spa</td><td>Rancho Santa Fe</td><td>—</td></tr>
</tbody></table>

#### Sacramento

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Sawyer Hotel by IHG</td><td>Sacramento</td><td>—</td></tr>
</tbody></table>

#### San Diego

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alma San Diego Downtown, a Tribute Portfolio Hotel</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Estancia La Jolla Hotel &amp; Spa</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Grand Del Mar</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental San Diego by IHG</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kona Kai San Diego</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry San Diego</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Torrey Pines</td><td>San Diego</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The US Grant, a Luxury Collection Hotel, San Diego</td><td>San Diego</td><td>—</td></tr>
</tbody></table>

#### San Francisco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel San Francisco</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont San Francisco</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel San Francisco</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel San Francisco at Embarcadero</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Zoe</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Palace Hotel, a Luxury Collection Hotel, San Francisco</td><td>San Francisco</td><td><a href="https://www.youtube.com/watch?v=USr5hpVl4k4">Video</a></td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>San Francisco Proper Hotel</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Taj Campton Place</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Jay, Autograph Collection</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, San Francisco</td><td>San Francisco</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis San Francisco</td><td>San Francisco</td><td>—</td></tr>
</tbody></table>

#### San Martin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>CordeValle</td><td>San Martin</td><td>—</td></tr>
</tbody></table>

#### Santa Barbara

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>El Encanto, Santa Barbara</td><td>Santa Barbara</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Californian</td><td>Santa Barbara</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Canary Hotel by IHG</td><td>Santa Barbara</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>San Ysidro Ranch</td><td>Santa Barbara</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Bacara, Santa Barbara</td><td>Santa Barbara</td><td>—</td></tr>
</tbody></table>

#### Santa Monica

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Miramar Hotel</td><td>Santa Monica</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Casa del Mar</td><td>Santa Monica</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Regent Santa Monica Beach</td><td>Santa Monica</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Santa Monica Proper Hotel, a Member of Design Hotels</td><td>Santa Monica</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shutters on the Beach</td><td>Santa Monica</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Pierside Santa Monica</td><td>Santa Monica</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Santa Monica</td><td>Santa Monica</td><td>—</td></tr>
</tbody></table>

#### Sausalito

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cavallo Point</td><td>Sausalito</td><td>—</td></tr>
</tbody></table>

#### Sonoma

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Sonoma Mission Inn &amp; Spa</td><td>Sonoma</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Macarthur Place</td><td>Sonoma</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Sonoma Resort, Autograph Collection</td><td>Sonoma</td><td>—</td></tr>
</tbody></table>

#### St. Helena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alila Napa Valley, a Hyatt Luxury Resort</td><td>St. Helena</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Auberge Du Soleil</td><td>St. Helena</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Meadowood Napa Valley</td><td>St. Helena</td><td>—</td></tr>
</tbody></table>

#### Thousand Oaks

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Los Angeles at Westlake Village</td><td>Thousand Oaks</td><td>—</td></tr>
</tbody></table>

#### West Hollywood

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel West Hollywood</td><td>West Hollywood</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton La Peer West Hollywood</td><td>West Hollywood</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sunset Marquis</td><td>West Hollywood</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sunset Tower Hotel</td><td>West Hollywood</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sun Rose West Hollywood</td><td>West Hollywood</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The West Hollywood EDITION</td><td>West Hollywood</td><td>—</td></tr>
</tbody></table>

#### Woodside

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canyon Ranch Woodside</td><td>Woodside</td><td>—</td></tr>
</tbody></table>

#### Yountville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bardessono Hotel and Spa</td><td>Yountville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Yountville</td><td>Yountville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Estate Yountville</td><td>Yountville</td><td>—</td></tr>
</tbody></table>

#### Aspen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Aspen Meadows Resort</td><td>Aspen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Hotel Aspen</td><td>Aspen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>MOLLIE Aspen</td><td>Aspen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Residences at the Little Nell</td><td>Aspen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Little Nell</td><td>Aspen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Aspen Resort</td><td>Aspen</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Aspen</td><td>Aspen</td><td>—</td></tr>
</tbody></table>

#### Avon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Bachelor Gulch</td><td>Avon</td><td>—</td></tr>
</tbody></table>

#### Beaver Creek

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Beaver Creek Resort &amp; Spa</td><td>Beaver Creek</td><td>—</td></tr>
</tbody></table>

#### Boulder

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Boulder</td><td>Boulder</td><td>—</td></tr>
</tbody></table>

#### Broomfield

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Interlocken Resort</td><td>Broomfield</td><td>—</td></tr>
</tbody></table>

#### Colorado Springs

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Polaris</td><td>Colorado Springs</td><td>—</td></tr>
</tbody></table>

#### Denver

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Denver</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Halcyon, a hotel in Cherry Creek, Denver</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Clio, a Luxury Collection Hotel, Denver Cherry Creek</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Claret Hotel by IHG</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Hotel Denver</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Crawford Hotel</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Rally Hotel at McGregor Square</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Denver</td><td>Denver</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Denver</td><td>Denver</td><td>—</td></tr>
</tbody></table>

#### Dolores

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dunton Hot Springs</td><td>Dolores</td><td>—</td></tr>
</tbody></table>

#### Gateway

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Gateway Canyons Resort, A Noble House Resort</td><td>Gateway</td><td>—</td></tr>
</tbody></table>

#### Keystone

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kindred Resort a RockResort</td><td>Keystone</td><td>—</td></tr>
</tbody></table>

#### Snowmass Village

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Hotel Snowmass</td><td>Snowmass Village</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Snowmass</td><td>Snowmass Village</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viewline Resort Snowmass, Autograph Collection</td><td>Snowmass Village</td><td>—</td></tr>
</tbody></table>

#### Telluride

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Relais &amp; Châteaux Lumière by Dunton</td><td>Telluride</td><td>—</td></tr>
</tbody></table>

#### Vail

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort and Residences Vail</td><td>Vail</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Vail</td><td>Vail</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sonnenalp</td><td>Vail</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hythe, a Luxury Collection Resort, Vail</td><td>Vail</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sebastian - Vail</td><td>Vail</td><td>—</td></tr>
</tbody></table>

#### Morris

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Winvian Farm</td><td>Morris</td><td>—</td></tr>
</tbody></table>

#### Wilmington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Quoin Hotel</td><td>Wilmington</td><td>—</td></tr>
</tbody></table>

#### Washington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Eaton DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Washington DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Washington D.C. - The Wharf by IHG</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Washington DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Washington DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Riggs Washington DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Salamander Washington DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel Washington DC Lafayette Square</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Dupont Circle Hotel</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hay-Adams</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Jefferson</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The LINE DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Georgetown, Washington, D.C.</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Washington, D.C.</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Washington, D.C.</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Watergate Hotel</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Washington DC</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Willard InterContinental Washington by IHG</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Yours Truly DC, Vignette Collection by IHG</td><td>Washington</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn at Little Washington</td><td>Washington</td><td>—</td></tr>
</tbody></table>

#### Amelia Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Amelia Island Resort</td><td>Amelia Island</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Amelia Island</td><td>Amelia Island</td><td>—</td></tr>
</tbody></table>

#### Aventura

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Turnberry Resort &amp; Spa</td><td>Aventura</td><td>—</td></tr>
</tbody></table>

#### Bal Harbour

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Bal Harbour, Miami</td><td>Bal Harbour</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Bal Harbour Resort</td><td>Bal Harbour</td><td>—</td></tr>
</tbody></table>

#### Boca Raton

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Beach Club at The Boca Raton</td><td>Boca Raton</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cloister at The Boca Raton</td><td>Boca Raton</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Tower at The Boca Raton</td><td>Boca Raton</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Yacht Club at The Boca Raton (Adults-only)</td><td>Boca Raton</td><td>—</td></tr>
</tbody></table>

#### Bonita Springs

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Coconut Point Resort &amp; Spa</td><td>Bonita Springs</td><td>—</td></tr>
</tbody></table>

#### ChampionsGate

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Orlando at Championsgate</td><td>ChampionsGate</td><td>—</td></tr>
</tbody></table>

#### Clearwater Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Clearwater Beach Resort &amp; Spa</td><td>Clearwater Beach</td><td>—</td></tr>
</tbody></table>

#### Delray Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Seagate Hotel and Spa</td><td>Delray Beach</td><td>—</td></tr>
</tbody></table>

#### Duck Key

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hawks Cay Resort &amp; Villas</td><td>Duck Key</td><td>—</td></tr>
</tbody></table>

#### Fort Lauderdale

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel and Residences Fort Lauderdale</td><td>Fort Lauderdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Fort Lauderdale Hotel</td><td>Fort Lauderdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pelican Grand Beach Resort - A Noble House Resort</td><td>Fort Lauderdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pier Sixty Six</td><td>Fort Lauderdale</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Fort Lauderdale</td><td>Fort Lauderdale</td><td>—</td></tr>
</tbody></table>

#### Key Largo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Playa Largo Resort &amp; Spa, Autograph Collection</td><td>Key Largo</td><td>—</td></tr>
</tbody></table>

#### Key West

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Marquesa Key West</td><td>Key West</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ocean Key Resort - A Noble House Resort</td><td>Key West</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Oceans Edge Resort &amp; Marina</td><td>Key West</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Perry Hotel &amp; Marina</td><td>Key West</td><td>—</td></tr>
</tbody></table>

#### Lake Buena Vista

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Orlando at WALT DISNEY WORLD® Resort</td><td>Lake Buena Vista</td><td>—</td></tr>
</tbody></table>

#### Little Torch Key

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Little Palm Island Resort &amp; Spa</td><td>Little Torch Key</td><td>—</td></tr>
</tbody></table>

#### Longboat Key

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Longboat Key Resort</td><td>Longboat Key</td><td>—</td></tr>
</tbody></table>

#### Marathon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Isla Bella Beach Resort &amp; Spa</td><td>Marathon</td><td>—</td></tr>
</tbody></table>

#### Marco Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Marco Island Beach Resort</td><td>Marco Island</td><td>—</td></tr>
</tbody></table>

#### Miami

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Miami</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Miami by IHG</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton EPIC Hotel by IHG</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mayfair House Hotel &amp; Garden - Coconut Grove Miami</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SLS Lux Brickell</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Coconut Grove, Miami</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Key Biscayne, Miami</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Shelborne by Proper</td><td>Miami</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Trump National Doral Miami</td><td>Miami</td><td>—</td></tr>
</tbody></table>

#### Miami Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel South Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Delano Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Eden Roc Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Faena Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fontainebleau Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Miami Beach Hotel</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SLS South Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lennox Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Miami Beach EDITION</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, South Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Setai, Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Standard Spa Miami Beach</td><td>Miami Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W South Beach</td><td>Miami Beach</td><td>—</td></tr>
</tbody></table>

#### Naples

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn on Fifth</td><td>Naples</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>LaPlaya Beach &amp; Golf Resort - A Noble House Resort</td><td>Naples</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Naples Beach Club, A Four Seasons Resort</td><td>Naples</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Naples, Tiburón</td><td>Naples</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Naples</td><td>Naples</td><td>—</td></tr>
</tbody></table>

#### Orlando

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Orlando Bonnet Creek Resort &amp; Spa</td><td>Orlando</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Orlando, Grande Lakes</td><td>Orlando</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lake Nona Wave Hotel</td><td>Orlando</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Orlando, Grande Lakes</td><td>Orlando</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Residences Orlando, Grande Lakes</td><td>Orlando</td><td>—</td></tr>
</tbody></table>

#### Palm Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amrit Ocean Resort</td><td>Palm Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Eau Resort &amp; Spa Palm Beach</td><td>Palm Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Palm Beach</td><td>Palm Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>PGA National Resort</td><td>Palm Beach</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ben, Autograph Collection</td><td>Palm Beach</td><td>—</td></tr>
</tbody></table>

#### Panama City Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Camp Creek Inn</td><td>Panama City Beach</td><td>—</td></tr>
</tbody></table>

#### St. Petersburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Vinoy Resort &amp; Golf Club, Autograph Collection</td><td>St. Petersburg</td><td>—</td></tr>
</tbody></table>

#### Sunny Isles Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Acqualina Resort &amp; Residences On The Beach</td><td>Sunny Isles Beach</td><td>—</td></tr>
</tbody></table>

#### Surfside

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel at The Surf Club</td><td>Surfside</td><td>—</td></tr>
</tbody></table>

#### Tampa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Tampa Water Street</td><td>Tampa</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Palihouse Hyde Park Village</td><td>Tampa</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Tampa EDITION</td><td>Tampa</td><td>—</td></tr>
</tbody></table>

#### Vero Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Vero Beach Hotel &amp; Spa by IHG</td><td>Vero Beach</td><td>—</td></tr>
</tbody></table>

#### Atlanta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>FORTH Hotel Atlanta</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Atlanta</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Colee, Atlanta Buckhead, Autograph Collection</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Buckhead Atlanta by IHG</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Shane Hotel by IHG</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Sylvan Hotel by IHG</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Atlanta Hotel</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Atlanta</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Hotel At The Battery Atlanta</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Atlanta</td><td>Atlanta</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Atlanta</td><td>Atlanta</td><td>—</td></tr>
</tbody></table>

#### Braselton

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Chateau Elan &amp; Winery</td><td>Braselton</td><td>—</td></tr>
</tbody></table>

#### Greensboro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Reynolds, Lake Oconee</td><td>Greensboro</td><td>—</td></tr>
</tbody></table>

#### Jekyll Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Jekyll Ocean Club</td><td>Jekyll Island</td><td>—</td></tr>
</tbody></table>

#### Savannah

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bardo Savannah</td><td>Savannah</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Brice Hotel by IHG</td><td>Savannah</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Perry Lane Hotel, a Luxury Collection Hotel, Savannah</td><td>Savannah</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Savannah</td><td>Savannah</td><td>—</td></tr>
</tbody></table>

#### Honolulu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>&#x27;Alohilani Resort Waikiki Beach</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Espacio The Jewel Of Waikiki</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moana Surfrider, A Westin Resort &amp; Spa, Waikiki Beach</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Kahala Hotel &amp; Resort</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Laylow Waikiki, Autograph Collection</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Residences, Waikiki Beach</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Royal Hawaiian, a Luxury Collection Resort, Waikiki</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waikiki Beach Marriott Resort &amp; Spa</td><td>Honolulu</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wayfinder Waikiki</td><td>Honolulu</td><td>—</td></tr>
</tbody></table>

#### Kahuku

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton O&#x27;ahu, Turtle Bay</td><td>Kahuku</td><td>—</td></tr>
</tbody></table>

#### Kailua-Kona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Hualalai</td><td>Kailua-Kona</td><td>—</td></tr>
</tbody></table>

#### Kapolei

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Oahu at Ko Olina</td><td>Kapolei</td><td>—</td></tr>
</tbody></table>

#### Kihei

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Maui at Wailea Resort</td><td>Kihei</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Kea Lani</td><td>Kihei</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Maui at Wailea</td><td>Kihei</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Wailea, Relais &amp; Châteaux</td><td>Kihei</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wailea Beach Resort - Marriott, Maui</td><td>Kihei</td><td>—</td></tr>
</tbody></table>

#### Kohala Coast

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Orchid, Hawaii</td><td>Kohala Coast</td><td>—</td></tr>
</tbody></table>

#### Koloa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Kauai Resort &amp; Spa</td><td>Koloa</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ko&#x27;a Kea Resort on Po&#x27;ipu Beach</td><td>Koloa</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Kukui’ula</td><td>Koloa</td><td>—</td></tr>
</tbody></table>

#### Lanai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Lanai</td><td>Lanai</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sensei Lanai, A Four Seasons Resort</td><td>Lanai</td><td>—</td></tr>
</tbody></table>

#### Princeville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Hanalei Bay</td><td>Princeville</td><td>—</td></tr>
</tbody></table>

#### West Maui

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Maui, Kapalua</td><td>West Maui</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Maui Resort &amp; Spa, Ka&#x27;anapali</td><td>West Maui</td><td>—</td></tr>
</tbody></table>

#### Ketchum

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Hotel Ketchum</td><td>Ketchum</td><td>—</td></tr>
</tbody></table>

#### Chicago

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Chicago Athletic Association, a Hyatt Hotel</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Chicago, Millennium Park</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Gray Hotel by IHG</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Chicago Hotel</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham, Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Peninsula Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Chicago</td><td>Chicago</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Chicago</td><td>Chicago</td><td>—</td></tr>
</tbody></table>

#### Indianapolis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Indianapolis</td><td>Indianapolis</td><td>—</td></tr>
</tbody></table>

#### Louisville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>21c Museum Hotel Louisville</td><td>Louisville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Genevieve</td><td>Louisville</td><td>—</td></tr>
</tbody></table>

#### New Orleans

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel New Orleans</td><td>New Orleans</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Fontenot by IHG</td><td>New Orleans</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Maison Métier</td><td>New Orleans</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, New Orleans</td><td>New Orleans</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Windsor Court</td><td>New Orleans</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels New Orleans</td><td>New Orleans</td><td>—</td></tr>
</tbody></table>

#### Kennebunkport

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hidden Pond Resort &amp; Tree Spa</td><td>Kennebunkport</td><td>—</td></tr>
</tbody></table>

#### Baltimore

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Baltimore</td><td>Baltimore</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Baltimore</td><td>Baltimore</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ivy Hotel</td><td>Baltimore</td><td>—</td></tr>
</tbody></table>

#### St. Michaels

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn at Perry Cabin</td><td>St. Michaels</td><td>—</td></tr>
</tbody></table>

#### Boston

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Boston Harbor Hotel</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Copley Plaza, Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel One Dalton Street, Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Commonwealth</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Boston Hotel at the Seaport</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Parker House</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Raffles Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham, Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Liberty, a Marriott Luxury Collection Hotel, Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Newbury Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Boston</td><td>Boston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>XV Beacon</td><td>Boston</td><td>—</td></tr>
</tbody></table>

#### Cambridge

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Marlowe Hotel by IHG</td><td>Cambridge</td><td>—</td></tr>
</tbody></table>

#### Cape Cod

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Chatham Bars Inn</td><td>Cape Cod</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Red Jacket Beach Resort</td><td>Cape Cod</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wequassett Resort and Golf Club</td><td>Cape Cod</td><td>—</td></tr>
</tbody></table>

#### Lenox

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canyon Ranch Lenox</td><td>Lenox</td><td>—</td></tr>
</tbody></table>

#### Lexington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn at Hastings Park</td><td>Lexington</td><td>—</td></tr>
</tbody></table>

#### Nantucket

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Wauwinet</td><td>Nantucket</td><td>—</td></tr>
</tbody></table>

#### Detroit

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shinola Hotel</td><td>Detroit</td><td>—</td></tr>
</tbody></table>

#### Minneapolis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Elliot Park Hotel, Autograph Collection</td><td>Minneapolis</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Minneapolis</td><td>Minneapolis</td><td>—</td></tr>
</tbody></table>

#### Wayzata

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hotel Landing</td><td>Wayzata</td><td>—</td></tr>
</tbody></table>

#### Kansas City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Kansas City</td><td>Kansas City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Fontaine Hotel</td><td>Kansas City</td><td>—</td></tr>
</tbody></table>

#### St. Louis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>21c Museum Hotel St Louis</td><td>St. Louis</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel St Louis</td><td>St. Louis</td><td>—</td></tr>
</tbody></table>

#### Big Sky

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Big Sky</td><td>Big Sky</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>One&amp;Only Moonlight Basin</td><td>Big Sky</td><td>—</td></tr>
</tbody></table>

#### Bozeman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Armory Hotel Bozeman by IHG</td><td>Bozeman</td><td>—</td></tr>
</tbody></table>

#### Greenough

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Paws Up Montana</td><td>Greenough</td><td>—</td></tr>
</tbody></table>

#### Philipsburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch at Rock Creek</td><td>Philipsburg</td><td>—</td></tr>
</tbody></table>

#### Omaha

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Cottonwood by IHG</td><td>Omaha</td><td>—</td></tr>
</tbody></table>

#### Las Vegas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ARIA Resort &amp; Casino</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ARIA Sky Suites</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bellagio Hotel and Casino</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Caesars Palace</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fontainebleau Las Vegas</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Las Vegas</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mandalay Bay Resort And Casino</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>MGM Grand Hotel &amp; Casino</td><td>Las Vegas</td><td><a href="https://www.youtube.com/watch?v=Br1hcq8983A">Video</a></td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Las Vegas at Caesars Palace</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park MGM Las Vegas</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SKYLOFTS at MGM Grand</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Cosmopolitan Las Vegas</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Reserve at Park MGM</td><td>Las Vegas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Vdara Hotel &amp; Spa</td><td>Las Vegas</td><td>—</td></tr>
</tbody></table>

#### Bretton Woods

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Mount Washington Resort</td><td>Bretton Woods</td><td>—</td></tr>
</tbody></table>

#### Asbury Park

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Asbury Ocean Club Hotel</td><td>Asbury Park</td><td>—</td></tr>
</tbody></table>

#### Cape May

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Beach Plum Farm Cottages</td><td>Cape May</td><td>—</td></tr>
</tbody></table>

#### Peapack

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Natirar</td><td>Peapack</td><td>—</td></tr>
</tbody></table>

#### Santa Fe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Rancho Encantado Santa Fe</td><td>Santa Fe</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn and Spa at Loretto</td><td>Santa Fe</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn of the Five Graces</td><td>Santa Fe</td><td>—</td></tr>
</tbody></table>

#### Accord

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inness</td><td>Accord</td><td>—</td></tr>
</tbody></table>

#### Amenia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Troutbeck</td><td>Amenia</td><td>—</td></tr>
</tbody></table>

#### Brooklyn

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Brooklyn Bridge</td><td>Brooklyn</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ace Hotel Brooklyn</td><td>Brooklyn</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The William Vale</td><td>Brooklyn</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wythe Hotel</td><td>Brooklyn</td><td>—</td></tr>
</tbody></table>

#### Canandaigua

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lake House on Canandaigua</td><td>Canandaigua</td><td>—</td></tr>
</tbody></table>

#### Chester

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Glenmere Mansion</td><td>Chester</td><td>—</td></tr>
</tbody></table>

#### Hunter

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Scribner&#x27;s Catskill Lodge</td><td>Hunter</td><td>—</td></tr>
</tbody></table>

#### Montauk

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Marram</td><td>Montauk</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montauk Yacht Club</td><td>Montauk</td><td>—</td></tr>
</tbody></table>

#### New York

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>33 Hotel, New York City, Seaport</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Baccarat Hotel New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Casa Cipriani New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Equinox Hotel New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Faena New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fouquet&#x27;s New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel New York Downtown</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Gansevoort Meatpacking</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental New York Barclay by IHG</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental New York Times Square by IHG</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Essex House New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Regency New York Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lotte New York Palace</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nine Orchard</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Lane New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Manhattan West</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Smyth Tribeca</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Soho Grand Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Beekman, A Thompson Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Chatwal, New York In The Unbound Collection By Hyatt</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Dominick</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Fifth Avenue Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham, New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The London, a Luxury Collection Hotel, New York City</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lowell Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Mark</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ned NoMad</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Peninsula New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Plaza, a Fairmont Managed Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton New York, Central Park</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton New York, NoMad</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Standard High Line</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Standard, East Village</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Surrey, A Corinthia Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Times Square EDITION</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Towers at Lotte New York Palace</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Twenty Two New York</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Wall Street Hotel</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Whitby</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Central Park</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels New York City</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W New York - Union Square</td><td>New York</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Warren Street</td><td>New York</td><td>—</td></tr>
</tbody></table>

#### Queens

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Rockaway Hotel &amp; Spa</td><td>Queens</td><td>—</td></tr>
</tbody></table>

#### Sloatsburg, NY

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch Hudson Valley</td><td>Sloatsburg, NY</td><td>—</td></tr>
</tbody></table>

#### The Hamptons

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canoe Place Inn &amp; Cottages</td><td>The Hamptons</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>EHP Resort &amp; Marina</td><td>The Hamptons</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Roundtree, Amagansett</td><td>The Hamptons</td><td>—</td></tr>
</tbody></table>

#### Asheville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Lodge Asheville, Autograph Collection®</td><td>Asheville</td><td>—</td></tr>
</tbody></table>

#### Chapel Hill

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Carolina Inn</td><td>Chapel Hill</td><td>—</td></tr>
</tbody></table>

#### Charlotte

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Tryon Park</td><td>Charlotte</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ballantyne, A Luxury Collection Hotel, Charlotte</td><td>Charlotte</td><td>—</td></tr>
</tbody></table>

#### Duck

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sanderling</td><td>Duck</td><td>—</td></tr>
</tbody></table>

#### Maggie Valley

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cataloochee Ranch</td><td>Maggie Valley</td><td>—</td></tr>
</tbody></table>

#### Pittsboro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Fearrington House</td><td>Pittsboro</td><td>—</td></tr>
</tbody></table>

#### Winston-Salem

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Cardinal Hotel by IHG</td><td>Winston-Salem</td><td>—</td></tr>
</tbody></table>

#### Cincinnati

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>21C Museum Hotel Cincinnati</td><td>Cincinnati</td><td>—</td></tr>
</tbody></table>

#### Cleveland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Cleveland</td><td>Cleveland</td><td>—</td></tr>
</tbody></table>

#### Columbus

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel LeVeque, Autograph Collection</td><td>Columbus</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Junto</td><td>Columbus</td><td>—</td></tr>
</tbody></table>

#### Oklahoma City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Oklahoma City Hotel</td><td>Oklahoma City</td><td>—</td></tr>
</tbody></table>

#### Dundee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Black Walnut Inn &amp; Vineyard</td><td>Dundee</td><td>—</td></tr>
</tbody></table>

#### Pacific City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Headlands Coastal Lodge &amp; Spa</td><td>Pacific City</td><td>—</td></tr>
</tbody></table>

#### Portland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Vintage Portland by IHG</td><td>Portland</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>RiverPlace Hotel</td><td>Portland</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Nines, a Luxury Collection Hotel, Portland</td><td>Portland</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Portland</td><td>Portland</td><td>—</td></tr>
</tbody></table>

#### Sunriver

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sunriver Resort</td><td>Sunriver</td><td>—</td></tr>
</tbody></table>

#### Philadelphia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Philadelphia at Comcast Center</td><td>Philadelphia</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Philadelphia Hotel</td><td>Philadelphia</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel Philadelphia at Rittenhouse Square</td><td>Philadelphia</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Rittenhouse Philadelphia</td><td>Philadelphia</td><td>—</td></tr>
</tbody></table>

#### Newport

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Brenton Hotel</td><td>Newport</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Castle Hill Inn</td><td>Newport</td><td>—</td></tr>
</tbody></table>

#### Richmond

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Preserve Sporting Club &amp; Resort</td><td>Richmond</td><td>—</td></tr>
</tbody></table>

#### Watch Hill

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ocean House</td><td>Watch Hill</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Weekapaug Inn</td><td>Watch Hill</td><td>—</td></tr>
</tbody></table>

#### Bluffton

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Palmetto Bluff</td><td>Bluffton</td><td>—</td></tr>
</tbody></table>

#### Charleston

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Emeline</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Charleston, Autograph Collection</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bennett</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Operis, Autograph Collection®</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Charleston Place</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Pinch Hotel</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ryder Hotel</td><td>Charleston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Zero George Street Hotel</td><td>Charleston</td><td>—</td></tr>
</tbody></table>

#### Hilton Head Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Hilton Head Oceanfront Resort</td><td>Hilton Head Island</td><td>—</td></tr>
</tbody></table>

#### Kiawah Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sanctuary at Kiawah Island Golf Resort</td><td>Kiawah Island</td><td>—</td></tr>
</tbody></table>

#### Franklin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Southall Farm &amp; Inn</td><td>Franklin</td><td>—</td></tr>
</tbody></table>

#### Nashville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Nashville</td><td>Nashville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Nashville</td><td>Nashville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Nashville Hotel at Vanderbilt Plaza</td><td>Nashville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Noelle</td><td>Nashville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hermitage Hotel</td><td>Nashville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Nashville, by Hyatt</td><td>Nashville</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels Nashville</td><td>Nashville</td><td>—</td></tr>
</tbody></table>

#### Austin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Austin Proper Hotel, a Member of Design Hotels</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Austin</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Austin</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Magdalena</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Van Zandt</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lake Austin Spa Resort – All-Inclusive, Adults Only</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The LINE Austin</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Austin, by Hyatt</td><td>Austin</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Austin</td><td>Austin</td><td>—</td></tr>
</tbody></table>

#### Dallas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Dallas</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hôtel Swexan</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Pittman Hotel – Downtown Dallas by IHG</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Adolphus, Autograph Collection</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Joule Dallas</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Dallas</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Dallas</td><td>Dallas</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels Dallas</td><td>Dallas</td><td>—</td></tr>
</tbody></table>

#### Houston

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Houston</td><td>Houston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Granduca Houston</td><td>Houston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Saint Augustine</td><td>Houston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Houston Grand Hotel - River Oaks</td><td>Houston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Post Oak Hotel at Uptown Houston</td><td>Houston</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Houston</td><td>Houston</td><td>—</td></tr>
</tbody></table>

#### Irving

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Dallas, Las Colinas</td><td>Irving</td><td>—</td></tr>
</tbody></table>

#### San Antonio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Emma at Pearl</td><td>San Antonio</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Hill Country Resort and Villas</td><td>San Antonio</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental San Antonio Riverwalk by IHG</td><td>San Antonio</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Santo San Antonio - Riverwalk by IHG</td><td>San Antonio</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson San Antonio River Walk</td><td>San Antonio</td><td>—</td></tr>
</tbody></table>

#### Heber City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Black Rock Mountain Resort</td><td>Heber City</td><td>—</td></tr>
</tbody></table>

#### Ivins

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Black Desert Resort</td><td>Ivins</td><td>—</td></tr>
</tbody></table>

#### Park City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Deer Valley</td><td>Park City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Deer Valley</td><td>Park City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Park City</td><td>Park City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Stein Eriksen Lodge</td><td>Park City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Stein Eriksen Residences</td><td>Park City</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Deer Valley</td><td>Park City</td><td>—</td></tr>
</tbody></table>

#### Salt Lake City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Monaco Salt Lake City by IHG</td><td>Salt Lake City</td><td>—</td></tr>
</tbody></table>

#### Sandy

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Snowpine Lodge</td><td>Sandy</td><td>—</td></tr>
</tbody></table>

#### Sundance

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sundance Mountain Resort</td><td>Sundance</td><td>—</td></tr>
</tbody></table>

#### Barnard

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Twin Farms</td><td>Barnard</td><td>—</td></tr>
</tbody></table>

#### Manchester

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Taconic Hotel by IHG</td><td>Manchester</td><td>—</td></tr>
</tbody></table>

#### Woodstock

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Woodstock Inn &amp; Resort</td><td>Woodstock</td><td>—</td></tr>
</tbody></table>

#### Arlington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Pentagon City</td><td>Arlington</td><td>—</td></tr>
</tbody></table>

#### Charlottesville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton The Forum Hotel by IHG</td><td>Charlottesville</td><td>—</td></tr>
</tbody></table>

#### Hot Springs

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Homestead Resort</td><td>Hot Springs</td><td>—</td></tr>
</tbody></table>

#### Irvington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Tides Inn</td><td>Irvington</td><td>—</td></tr>
</tbody></table>

#### Keswick

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Keswick Hall &amp; Golf Club</td><td>Keswick</td><td>—</td></tr>
</tbody></table>

#### McLean

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Tysons Corner</td><td>McLean</td><td>—</td></tr>
</tbody></table>

#### Middleburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Salamander Middleburg</td><td>Middleburg</td><td>—</td></tr>
</tbody></table>

#### Bellevue

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Seattle Bellevue, by IHG</td><td>Bellevue</td><td>—</td></tr>
</tbody></table>

#### Seattle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Seattle</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Olympic Hotel</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Seattle</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Palladian Hotel</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lotte Hotel Seattle</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Edgewater Hotel</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The State Hotel</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Seattle</td><td>Seattle</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Seattle</td><td>Seattle</td><td>—</td></tr>
</tbody></table>

#### Kohler

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The American Club</td><td>Kohler</td><td>—</td></tr>
</tbody></table>

#### Milwaukee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Journeyman Hotel by IHG</td><td>Milwaukee</td><td>—</td></tr>
</tbody></table>

#### Jackson Hole

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Jackson Hole</td><td>Jackson Hole</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Terra Jackson Hole - A Noble House Resort</td><td>Jackson Hole</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Teton Mountain Lodge and Spa</td><td>Jackson Hole</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Cabins At Snake River Sporting Club</td><td>Jackson Hole</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Cloudveil, Autograph Collection</td><td>Jackson Hole</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sylvan Lodge at Snake River Sporting Club</td><td>Jackson Hole</td><td>—</td></tr>
</tbody></table>

#### Saratoga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Brush Creek Ranch</td><td>Saratoga</td><td>—</td></tr>
</tbody></table>

## Caribbean

### Anguilla

#### Anguilla

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Aurora Anguilla Resort &amp; Golf Club</td><td>Anguilla</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Cap Juluca, A Belmond Hotel</td><td>Anguilla</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Four Seasons Resort and Residences Anguilla</td><td>Anguilla</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Malliouhana Resort Anguilla</td><td>Anguilla</td><td>—</td></tr>
</tbody></table>

### Antigua & Barbuda

#### Antigua

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua &amp; Barbuda"><td>Carlisle Bay</td><td>Antigua</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua &amp; Barbuda"><td>Jumby Bay Island, Oetker Hotels</td><td>Antigua</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua &amp; Barbuda"><td>The Inn at English Harbour</td><td>Antigua</td><td>—</td></tr>
</tbody></table>

### Aruba

#### Aruba

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>Hyatt Regency Aruba Resort Spa &amp; Casino</td><td>Aruba</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>The Ritz-Carlton, Aruba</td><td>Aruba</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>The St. Regis Aruba Resort</td><td>Aruba</td><td>—</td></tr>
</tbody></table>

### Bahamas

#### Eleuthera

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>Pink Sands Resort</td><td>Eleuthera</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Cove Eleuthera</td><td>Eleuthera</td><td>—</td></tr>
</tbody></table>

#### Nassau

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>Grand Hyatt Baha Mar</td><td>Nassau</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>SLS Baha Mar</td><td>Nassau</td><td>—</td></tr>
</tbody></table>

#### Paradise Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Cove at Atlantis</td><td>Paradise Island</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Ocean Club, A Four Seasons Resort, Bahamas</td><td>Paradise Island</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Reef at Atlantis</td><td>Paradise Island</td><td>—</td></tr>
</tbody></table>

### Barbados

#### Barbados

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Barbados"><td>Fairmont Royal Pavilion</td><td>Barbados</td><td>—</td></tr>
</tbody></table>

### Bermuda

#### Bermuda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>Hamilton Princess &amp; Beach Club - A Fairmont Hotel</td><td>Bermuda</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>The Loren at Pink Beach</td><td>Bermuda</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>The St. Regis Bermuda Resort</td><td>Bermuda</td><td>—</td></tr>
</tbody></table>

### Cayman Islands

#### Grand Cayman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Grand Hyatt Grand Cayman Resort &amp; Spa</td><td>Grand Cayman</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Hotel Indigo Grand Cayman</td><td>Grand Cayman</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Kimpton Seafire Resort + Spa by IHG</td><td>Grand Cayman</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>The Ritz-Carlton, Grand Cayman</td><td>Grand Cayman</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>The Westin Grand Cayman Seven Mile Beach Resort &amp; Spa</td><td>Grand Cayman</td><td>—</td></tr>
</tbody></table>

### Dominica

#### Dominica

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominica"><td>Intercontinental Dominica Cabrits Resort &amp; Spa</td><td>Dominica</td><td>—</td></tr>
</tbody></table>

### Dominican Republic

#### La Romana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Casa de Campo Resort and Villas</td><td>La Romana</td><td>—</td></tr>
</tbody></table>

#### Punta Cana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Eden Roc Cap Cana</td><td>Punta Cana</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Paradisus Palma Real Golf &amp; Spa Resort All Inclusive</td><td>Punta Cana</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>The St. Regis Cap Cana Resort</td><td>Punta Cana</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Tortuga Bay Hotel</td><td>Punta Cana</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Zel Punta Cana All Suites</td><td>Punta Cana</td><td>—</td></tr>
</tbody></table>

#### Santo Domingo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Kimpton Las Mercedes by IHG</td><td>Santo Domingo</td><td>—</td></tr>
</tbody></table>

### Grenada

#### Grenada

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada"><td>Calabash Hotel</td><td>Grenada</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada"><td>Six Senses La Sagesse Grenada</td><td>Grenada</td><td>—</td></tr>
</tbody></table>

### Jamaica

#### Montego Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>Half Moon</td><td>Montego Bay</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>Round Hill Hotel &amp; Villas</td><td>Montego Bay</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>S Hotel Montego Bay</td><td>Montego Bay</td><td>—</td></tr>
</tbody></table>

### Puerto Rico

#### Dorado

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Dorado Beach, a Ritz-Carlton Reserve</td><td>Dorado</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Residences at Dorado Beach, a Ritz-Carlton Reserve</td><td>Dorado</td><td>—</td></tr>
</tbody></table>

#### Río Grande

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Four Seasons Resort and Residences Puerto Rico</td><td>Río Grande</td><td>—</td></tr>
</tbody></table>

#### San Juan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Condado Vanderbilt Hotel</td><td>San Juan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Fairmont El San Juan Hotel</td><td>San Juan</td><td>—</td></tr>
</tbody></table>

### St. Barthélemy

#### St. Barthelemy

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy"><td>Fouquet&#x27;s Saint-Barth</td><td>St. Barthelemy</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy"><td>Hotel Le Toiny</td><td>St. Barthelemy</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy"><td>Le Barthélemy Hotel &amp; Spa</td><td>St. Barthelemy</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Barthélemy"><td>Le Sereno</td><td>St. Barthelemy</td><td>—</td></tr>
</tbody></table>

### St. Kitts & Nevis

#### St. Kitts & Nevis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Kitts &amp; Nevis"><td>Four Seasons Resort - Nevis</td><td>St. Kitts &amp; Nevis</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Kitts &amp; Nevis"><td>Park Hyatt St. Kitts</td><td>St. Kitts &amp; Nevis</td><td>—</td></tr>
</tbody></table>

### St. Lucia

#### St. Lucia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Lucia"><td>Cap Maison Resort &amp; Spa</td><td>St. Lucia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Lucia"><td>Sugar Beach, A Viceroy Resort</td><td>St. Lucia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Lucia"><td>Zoetry Marigot Bay St. Lucia</td><td>St. Lucia</td><td>—</td></tr>
</tbody></table>

### St. Martin

#### St. Martin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="St. Martin"><td>La Samanna, A Belmond Hotel, St. Martin</td><td>St. Martin</td><td>—</td></tr>
</tbody></table>

### Turks & Caicos Islands

#### Parrot Cay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>COMO Parrot Cay</td><td>Parrot Cay</td><td>—</td></tr>
</tbody></table>

#### Providenciales

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>Beach Enclave</td><td>Providenciales</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>Grace Bay Club</td><td>Providenciales</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>Rock House</td><td>Providenciales</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>South Bank</td><td>Providenciales</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>The Ritz-Carlton, Turks &amp; Caicos</td><td>Providenciales</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>Wymara Resort and Villas</td><td>Providenciales</td><td>—</td></tr>
</tbody></table>

#### South Caicos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks &amp; Caicos Islands"><td>Salterra, a Luxury Collection Resort &amp; Spa, South Caicos</td><td>South Caicos</td><td>—</td></tr>
</tbody></table>

### U.S. Virgin Islands

#### St. Thomas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands"><td>Buoy Haus Beach Resort St. Thomas, Autograph Collection</td><td>St. Thomas</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands"><td>The Ritz-Carlton, St. Thomas</td><td>St. Thomas</td><td>—</td></tr>
</tbody></table>

## Central & South America

### Argentina

#### Buenos Aires

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Faena Hotel Buenos Aires</td><td>Buenos Aires</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Four Seasons Hotel Buenos Aires</td><td>Buenos Aires</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Palacio Duhau - Park Hyatt Buenos Aires</td><td>Buenos Aires</td><td>—</td></tr>
</tbody></table>

#### Puerto Iguazú

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Awasi Iguazú</td><td>Puerto Iguazú</td><td>—</td></tr>
</tbody></table>

#### Uco Valley

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>The Vines Resort &amp; Spa</td><td>Uco Valley</td><td>—</td></tr>
</tbody></table>

### Belize

#### Ambergris Caye

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize"><td>Alaia Belize, Autograph Collection</td><td>Ambergris Caye</td><td>—</td></tr>
</tbody></table>

#### Placencia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize"><td>Itz’ana Resort &amp; Residences, Placencia</td><td>Placencia</td><td>—</td></tr>
</tbody></table>

### Brazil

#### Foz do Iguaçu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Hotel das Cataratas, A Belmond Hotel, Iguassu Falls</td><td>Foz do Iguaçu</td><td>—</td></tr>
</tbody></table>

#### Rio de Janeiro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Copacabana Palace, A Belmond Hotel, Rio de Janeiro</td><td>Rio de Janeiro</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Fairmont Rio de Janeiro Copacabana</td><td>Rio de Janeiro</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Santa Teresa Hotel Rio de Janeiro - MGallery Collection</td><td>Rio de Janeiro</td><td>—</td></tr>
</tbody></table>

#### São Paulo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>InterContinental São Paulo by IHG</td><td>São Paulo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Palacio Tangara, Oetker Hotels</td><td>São Paulo</td><td>—</td></tr>
</tbody></table>

### Chile

#### Santiago

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>The Ritz-Carlton, Santiago</td><td>Santiago</td><td>—</td></tr>
</tbody></table>

### Colombia

#### Bogotá

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Four Seasons Hotel Bogota</td><td>Bogotá</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Four Seasons Hotel Bogotá Casa Medina</td><td>Bogotá</td><td>—</td></tr>
</tbody></table>

#### Cartagena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Casa Pestagua Relais Châteaux</td><td>Cartagena</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>InterContinental Cartagena De Indias by IHG</td><td>Cartagena</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Sofitel Legend Santa Clara Cartagena</td><td>Cartagena</td><td>—</td></tr>
</tbody></table>

#### Cartagena de Indias

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Sofitel Barú Cartagena Beach Resort</td><td>Cartagena de Indias</td><td>—</td></tr>
</tbody></table>

### Costa Rica

#### La Fortuna

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nayara Gardens</td><td>La Fortuna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nayara Springs - Adults only</td><td>La Fortuna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nayara Tented Camp</td><td>La Fortuna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Tabacón Thermal Resort &amp; Spa</td><td>La Fortuna</td><td>—</td></tr>
</tbody></table>

#### Manuel Antonio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Los Altos Resort</td><td>Manuel Antonio</td><td>—</td></tr>
</tbody></table>

#### Papagayo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nekajui Peninsula Papagayo, a Ritz-Carlton Reserve Residence</td><td>Papagayo</td><td>—</td></tr>
</tbody></table>

#### Peninsula Papagayo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Andaz Peninsula Papagayo Resort, Costa Rica</td><td>Peninsula Papagayo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Four Seasons Resort Peninsula Papagayo, Costa Rica</td><td>Peninsula Papagayo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nekajui Peninsula Papagayo, a Ritz-Carlton Reserve</td><td>Peninsula Papagayo</td><td>—</td></tr>
</tbody></table>

#### Playa Conchal

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>W Costa Rica - Reserva Conchal</td><td>Playa Conchal</td><td>—</td></tr>
</tbody></table>

#### Santa Teresa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Hotel Nantipa - A Tico Beach Experience</td><td>Santa Teresa</td><td>—</td></tr>
</tbody></table>

### Honduras

#### Roatán

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Honduras"><td>Kimpton Grand Roatan Resort And Spa by IHG</td><td>Roatán</td><td>—</td></tr>
</tbody></table>

### Panama

#### Panama City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>Sofitel Legend Casco Viejo, Panama City</td><td>Panama City</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>The Santa Maria, a Luxury Collection Hotel &amp; Golf Resort, Panama City</td><td>Panama City</td><td>—</td></tr>
</tbody></table>

### Peru

#### Arequipa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Las Casitas, A Belmond Hotel</td><td>Arequipa</td><td>—</td></tr>
</tbody></table>

#### Cusco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Monasterio, A Belmond Hotel, Cusco</td><td>Cusco</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Palacio Nazarenas, A Belmond Hotel, Cusco</td><td>Cusco</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Rio Sagrado, A Belmond Hotel, Sacred Valley</td><td>Cusco</td><td><a href="https://www.youtube.com/watch?v=ZsNwOFKryvw">Video</a></td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Sanctuary Lodge, A Belmond Hotel, Machu Picchu</td><td>Cusco</td><td>—</td></tr>
</tbody></table>

#### Lima

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Miraflores Park, A Belmond Hotel, Lima</td><td>Lima</td><td>—</td></tr>
</tbody></table>

## Europe

### Austria

#### Salzburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Goldener Hirsch, a Luxury Collection Hotel, Salzburg</td><td>Salzburg</td><td>—</td></tr>
</tbody></table>

#### Vienna

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Almanac Palais Vienna</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Anantara Palais Hansen Vienna Hotel</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Imperial, a Luxury Collection Hotel, Vienna</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Sacher Wien</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Park Hyatt Vienna</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>SO/ Vienna</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>The Amauris Vienna - Relais &amp; Châteaux</td><td>Vienna</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>The Ritz-Carlton, Vienna</td><td>Vienna</td><td>—</td></tr>
</tbody></table>

### Belgium

#### Antwerp

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Botanic Sanctuary Antwerp - The Leading Hotels of the World</td><td>Antwerp</td><td>—</td></tr>
</tbody></table>

#### Brussels

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Corinthia Grand Hotel Astoria, Brussels</td><td>Brussels</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Hotel Amigo, a Rocco Forte hotel</td><td>Brussels</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Le Louise Hotel Brussels - MGallery</td><td>Brussels</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Sofitel Brussels Europe</td><td>Brussels</td><td>—</td></tr>
</tbody></table>

### Croatia

#### Dubrovnik

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Sun Gardens Dubrovnik</td><td>Dubrovnik</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Villa Dubrovnik</td><td>Dubrovnik</td><td>—</td></tr>
</tbody></table>

#### Hvar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Maslina Resort</td><td>Hvar</td><td>—</td></tr>
</tbody></table>

#### Pula

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Grand Hotel Brioni Pula A Radisson Collection Hotel</td><td>Pula</td><td>—</td></tr>
</tbody></table>

#### Split

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Radisson Blu Resort &amp; Spa, Split</td><td>Split</td><td>—</td></tr>
</tbody></table>

### Cyprus

#### Limassol

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Cyprus"><td>Parklane, a Luxury Collection Resort &amp; Spa, Limassol</td><td>Limassol</td><td>—</td></tr>
</tbody></table>

### Czechia

#### Prague

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Czechia"><td>Andaz Prague</td><td>Prague</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czechia"><td>Augustine, a Luxury Collection Hotel, Prague</td><td>Prague</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czechia"><td>Four Seasons Hotel Prague</td><td>Prague</td><td>—</td></tr>
</tbody></table>

### Denmark

#### Copenhagen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>NH Collection Copenhagen</td><td>Copenhagen</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>Nimb Hotel</td><td>Copenhagen</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>Nobis Hotel Copenhagen, a Member of Design Hotels</td><td>Copenhagen</td><td>—</td></tr>
</tbody></table>

### Finland

#### Helsinki

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Finland"><td>Hotel NH Collection Helsinki Grand Hansa</td><td>Helsinki</td><td>—</td></tr>
</tbody></table>

### France

#### Aix-en-Provence

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Château de Fonscolombe</td><td>Aix-en-Provence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Villa Gallici Hôtel &amp; Spa - Relais &amp; Châteaux</td><td>Aix-en-Provence</td><td>—</td></tr>
</tbody></table>

#### Avignon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Mirande</td><td>Avignon</td><td>—</td></tr>
</tbody></table>

#### Blois

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Fleur de Loire</td><td>Blois</td><td>—</td></tr>
</tbody></table>

#### Bonnieux

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Capelongue, a Beaumier Hotel</td><td>Bonnieux</td><td>—</td></tr>
</tbody></table>

#### Bordeaux

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Bordeaux - Le Grand Hotel</td><td>Bordeaux</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Mondrian Bordeaux Les Carmes</td><td>Bordeaux</td><td>—</td></tr>
</tbody></table>

#### Cannes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Carlton Cannes, a Regent Hotel</td><td>Cannes</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Five Seas by Inwood Hotels</td><td>Cannes</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hôtel Barrière Le Majestic Cannes</td><td>Cannes</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Martinez</td><td>Cannes</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Mondrian Cannes</td><td>Cannes</td><td>—</td></tr>
</tbody></table>

#### Flayosc

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Château De Berne</td><td>Flayosc</td><td>—</td></tr>
</tbody></table>

#### Guainville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine de Primard</td><td>Guainville</td><td>—</td></tr>
</tbody></table>

#### La Chapelle-en-Serval

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Chantilly Chateau Mont Royal by IHG</td><td>La Chapelle-en-Serval</td><td>—</td></tr>
</tbody></table>

#### Luberon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Coquillade Provence</td><td>Luberon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine de Fontenille</td><td>Luberon</td><td>—</td></tr>
</tbody></table>

#### Lyon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cour des Loges Lyon, A Radisson Collection Hotel</td><td>Lyon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Lyon - Hotel Dieu</td><td>Lyon</td><td>—</td></tr>
</tbody></table>

#### Marseille

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Marseille - Hotel Dieu by IHG</td><td>Marseille</td><td>—</td></tr>
</tbody></table>

#### Megève

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Four Seasons Resort Megeve</td><td>Megève</td><td>—</td></tr>
</tbody></table>

#### Nice

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Anantara Plaza Nice Hotel</td><td>Nice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Du Couvent, A Luxury Collection Hotel, Nice, France</td><td>Nice</td><td>—</td></tr>
</tbody></table>

#### Paris

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Bulgari Hotel Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Castille Paris – Starhotels Collezione</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cheval Blanc Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Fauchon L&#x27;Hotel Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Four Seasons Hotel George V</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Grand Hôtel du Palais Royal</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Balzac Paris &amp; Spa Ikoï</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hôtel Fouquet&#x27;s Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hôtel Plaza Athénée - Dorchester Collection</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Paris le Grand</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>J.K. Place Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Kimpton St Honore Paris by IHG</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Fantaisie</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Reserve Paris Hotel and Spa</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Bristol Paris, Oetker Hotels</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Meurice - Dorchester Collection</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Royal Monceau - Raffles Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Delano Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Park Hyatt Paris-Vendôme</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Pavillon de la Reine &amp; Spa, Place des Vosges</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Pavillon Faubourg Saint-Germain</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Relais Christine</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Ritz Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Saint James Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Shangri-La Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>SO/ Paris</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Paris Baltimore Tour Eiffel Hotel</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Paris Le Faubourg</td><td>Paris</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>The Peninsula Paris</td><td>Paris</td><td>—</td></tr>
</tbody></table>

#### Puligny-Montrachet

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>COMO Le Montrachet</td><td>Puligny-Montrachet</td><td>—</td></tr>
</tbody></table>

#### Roquebrune-Cap-Martin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Monte-Carlo Beach Hotel</td><td>Roquebrune-Cap-Martin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>The Maybourne Riviera, Maybourne</td><td>Roquebrune-Cap-Martin</td><td>—</td></tr>
</tbody></table>

#### Saint-Jean-Cap-Ferrat

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Grand-Hôtel du Cap-Ferrat, A Four Seasons Hotel</td><td>Saint-Jean-Cap-Ferrat</td><td>—</td></tr>
</tbody></table>

### Germany

#### Baden-Baden

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Brenners Park-Hotel &amp; Spa, Oetker Hotels</td><td>Baden-Baden</td><td>—</td></tr>
</tbody></table>

#### Berlin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Das Stue</td><td>Berlin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel De Rome Berlin</td><td>Berlin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Regent Berlin</td><td>Berlin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Ritz-Carlton, Berlin</td><td>Berlin</td><td>—</td></tr>
</tbody></table>

#### Cologne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Excelsior Hotel Ernst am Dom</td><td>Cologne</td><td>—</td></tr>
</tbody></table>

#### Frankfurt

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Kimpton Main Frankfurt by IHG</td><td>Frankfurt</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Sofitel Frankfurt Opera</td><td>Frankfurt</td><td>—</td></tr>
</tbody></table>

#### Hamburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Fairmont Hotel Vier Jahreszeiten Hamburg</td><td>Hamburg</td><td>—</td></tr>
</tbody></table>

#### Munich

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Koenigshof, A Luxury Collection Hotel, Munich</td><td>Munich</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Rocco Forte The Charles Hotel</td><td>Munich</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Sofitel Munich Bayerpost</td><td>Munich</td><td>—</td></tr>
</tbody></table>

### Greece

#### Agios Nikolaos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes of Elounda, Autograph Collection</td><td>Agios Nikolaos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Elounda Mare Relais &amp; Chateaux Hotel</td><td>Agios Nikolaos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>InterContinental Crete by IHG</td><td>Agios Nikolaos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Minos Beach Art Hotel</td><td>Agios Nikolaos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Phāea Blue - Small Luxury Hotels of the World</td><td>Agios Nikolaos</td><td>—</td></tr>
</tbody></table>

#### Athens

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Academias Hotel, Autograph Collection</td><td>Athens</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Athenaeum InterContinental by IHG</td><td>Athens</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Athens Capital Center Hotel</td><td>Athens</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Hotel Grande Bretagne, a Luxury Collection Hotel, Athens</td><td>Athens</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>King George, a Luxury Collection Hotel, Athens</td><td>Athens</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>New Hotel</td><td>Athens</td><td>—</td></tr>
</tbody></table>

#### Chania

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Noruz Chania, Autograph Collection - Adults Only</td><td>Chania</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Zeen Chania, a Luxury Collection Resort, Crete</td><td>Chania</td><td>—</td></tr>
</tbody></table>

#### Costa Navarino

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>The Romanos, a Luxury Collection Resort, Costa Navarino</td><td>Costa Navarino</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>W Costa Navarino</td><td>Costa Navarino</td><td>—</td></tr>
</tbody></table>

#### Glyfada

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>One&amp;Only Aesthesis</td><td>Glyfada</td><td>—</td></tr>
</tbody></table>

#### Halkidiki

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>The Danai</td><td>Halkidiki</td><td>—</td></tr>
</tbody></table>

#### Heraklion

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Amirandes, Grecotel Boutique Resort</td><td>Heraklion</td><td>—</td></tr>
</tbody></table>

#### Hersonissos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Phāea Cretan Malia, a Member of Design Hotels</td><td>Hersonissos</td><td>—</td></tr>
</tbody></table>

#### Kea

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>One&amp;Only Kéa Island</td><td>Kea</td><td>—</td></tr>
</tbody></table>

#### Mykonos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Bill &amp; Coo Mykonos</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Deos Mykonos</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Kouros Hotel &amp; Suites</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian Ambassador Hotel Relais &amp; Chateaux</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian Kyma, a member of Design Hotels</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian Villa Collection</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mykonos Blu, A Grecotel Resort to Live</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mykonos Grand Hotel &amp; Resort</td><td>Mykonos</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Santa Marina, a Luxury Collection Resort, Mykonos</td><td>Mykonos</td><td>—</td></tr>
</tbody></table>

#### Naousa Paros

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Avant Mar</td><td>Naousa Paros</td><td>—</td></tr>
</tbody></table>

#### Paros

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Cosme, A Luxury Collection Resort, Paros</td><td>Paros</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Parilio, a Member of Design Hotels</td><td>Paros</td><td>—</td></tr>
</tbody></table>

#### Paros Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Andronis Minois</td><td>Paros Island</td><td>—</td></tr>
</tbody></table>

#### Rethymno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Caramel, Grecotel Boutique Resort</td><td>Rethymno</td><td>—</td></tr>
</tbody></table>

#### Santorini

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Canaves Epitome - Small Luxury Hotels of the World</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Canaves Oia Suites - Small Luxury Hotels of the World</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Garden Santorini - The Leading Hotels Of The World</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Santorini - The Leading Hotels of the world</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Santorini – Pelagos House - The Leading Hotels of the World</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Magma Resort Santorini, part of The Unbound Collection by Hyatt</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mystique, a Luxury Collection Hotel, Santorini</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Nobu Hotel Santorini</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>NOŪS Santorini</td><td>Santorini</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Santo Pure Oia Suites &amp; Villas</td><td>Santorini</td><td>—</td></tr>
</tbody></table>

#### Sparta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Euphoria Retreat, Mystras</td><td>Sparta</td><td>—</td></tr>
</tbody></table>

#### Vari-Voula-Vouliagmeni

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Four Seasons Astir Palace Hotel Athens</td><td>Vari-Voula-Vouliagmeni</td><td>—</td></tr>
</tbody></table>

#### Zakynthos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Olea All Suite Hotel, a Member of Design Hotels</td><td>Zakynthos</td><td>—</td></tr>
</tbody></table>

### Hungary

#### Budapest

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Al Habtoor Palace Budapest, Preferred Hotels &amp; Resorts</td><td>Budapest</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Anantara New York Palace Budapest - A Leading Hotel of the World</td><td>Budapest</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Corinthia Budapest</td><td>Budapest</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Dorothea Hotel, Budapest, Autograph Collection</td><td>Budapest</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Four Seasons Gresham Palace</td><td>Budapest</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Kimpton BEM Budapest by IHG</td><td>Budapest</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Párisi Udvar Hotel Budapest</td><td>Budapest</td><td>—</td></tr>
</tbody></table>

### Iceland

#### Reykjavik

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Iceland"><td>The Reykjavik EDITION</td><td>Reykjavik</td><td>—</td></tr>
</tbody></table>

### Ireland

#### Adare

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Adare Manor</td><td>Adare</td><td>—</td></tr>
</tbody></table>

#### Ballyfin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Ballyfin Demesne</td><td>Ballyfin</td><td>—</td></tr>
</tbody></table>

#### Cong

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Ashford Castle</td><td>Cong</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Lodge at Ashford Castle</td><td>Cong</td><td>—</td></tr>
</tbody></table>

#### Cork

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The River Lee Hotel</td><td>Cork</td><td>—</td></tr>
</tbody></table>

#### Dublin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Anantara The Marker Hotel Dublin Hotel</td><td>Dublin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Dylan Hotel</td><td>Dublin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>InterContinental Dublin by IHG</td><td>Dublin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Fitzwilliam Hotel</td><td>Dublin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Merrion Hotel</td><td>Dublin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Shelbourne, Autograph Collection</td><td>Dublin</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Westbury Dublin</td><td>Dublin</td><td>—</td></tr>
</tbody></table>

#### Galway

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Glenlo Abbey Hotel</td><td>Galway</td><td>—</td></tr>
</tbody></table>

#### Kenmare

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Park Hotel Kenmare</td><td>Kenmare</td><td>—</td></tr>
</tbody></table>

#### Maynooth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Carton House, A Fairmont Hotel</td><td>Maynooth</td><td>—</td></tr>
</tbody></table>

#### Newmarket-on-Fergus

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Dromoland Castle</td><td>Newmarket-on-Fergus</td><td>—</td></tr>
</tbody></table>

### Italy

#### Amalfi Coast

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Caruso, A Belmond Hotel, Amalfi Coast</td><td>Amalfi Coast</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Angelina</td><td>Amalfi Coast</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Villa Franca Positano</td><td>Amalfi Coast</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il San Pietro di Positano</td><td>Amalfi Coast</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Santa Caterina</td><td>Amalfi Coast</td><td>—</td></tr>
</tbody></table>

#### Bagno a Ripoli

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa La Massa</td><td>Bagno a Ripoli</td><td>—</td></tr>
</tbody></table>

#### Barberino Tavarnelle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>COMO Castello Del Nero</td><td>Barberino Tavarnelle</td><td>—</td></tr>
</tbody></table>

#### Capri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Quisisana</td><td>Capri</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel La Palma, Oetker Hotels</td><td>Capri</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>J.K. Place Capri</td><td>Capri</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Jumeirah Capri Palace</td><td>Capri</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Marina Capri Hotel &amp; Spa</td><td>Capri</td><td>—</td></tr>
</tbody></table>

#### Cortina d'Ampezzo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Ancora Cortina</td><td>Cortina d&#x27;Ampezzo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Savoia Cortina d&#x27;Ampezzo, A Radisson Collection Hotel</td><td>Cortina d&#x27;Ampezzo</td><td>—</td></tr>
</tbody></table>

#### Costa Smeralda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>7Pines Resort Sardinia</td><td>Costa Smeralda</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Cala di Volpe, a Luxury Collection Hotel, Costa Smeralda</td><td>Costa Smeralda</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>CPH Pevero Hotel</td><td>Costa Smeralda</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Romazzino, A Belmond Hotel, Costa Smeralda</td><td>Costa Smeralda</td><td>—</td></tr>
</tbody></table>

#### Courmayeur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Courmayeur Montblanc by R Collection Hotels</td><td>Courmayeur</td><td>—</td></tr>
</tbody></table>

#### Fasano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo Egnazia</td><td>Fasano</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Masseria Torre Maizza</td><td>Fasano</td><td>—</td></tr>
</tbody></table>

#### Fiesole

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa San Michele, A Belmond Hotel, Florence</td><td>Fiesole</td><td>—</td></tr>
</tbody></table>

#### Florence

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Four Seasons Hotel Firenze</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Helvetia &amp; Bristol Firenze – Starhotels Collezione</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Lungarno - Lungarno Collection</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Regency, Florence</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>IL Tornabuoni, part of the Unbound Collection by Hyatt</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Portrait Firenze - Lungarno Collection</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Hotel Savoy</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Sina Villa Medici, Autograph Collection</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Excelsior, a Luxury Collection Hotel, Florence</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Place Firenze</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The St. Regis Florence</td><td>Florence</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Cora</td><td>Florence</td><td>—</td></tr>
</tbody></table>

#### Lake Como

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Tremezzo, Lake Como</td><td>Lake Como</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Victoria Concept &amp; Spa, by R Collection Hotels</td><td>Lake Como</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il Sereno Lake Como</td><td>Lake Como</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Venezia</td><td>Lake Como</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Passalacqua</td><td>Lake Como</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa d&#x27;Este</td><td>Lake Como</td><td>—</td></tr>
</tbody></table>

#### Lake Garda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Lefay Resort &amp; SPA Lago Di Garda</td><td>Lake Garda</td><td>—</td></tr>
</tbody></table>

#### Langhe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa di Langa</td><td>Langhe</td><td>—</td></tr>
</tbody></table>

#### Maratea

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il Santavenere</td><td>Maratea</td><td>—</td></tr>
</tbody></table>

#### Milan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Bulgari Hotel Milano</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Brera, a Luxury Collection Hotel, Milan</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Cipriani Milano</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Four Seasons Hotel Milano</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel et de Milan</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Principe Di Savoia</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>ME Milan il Duca</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Touring Club Milan, A Radisson Collection Hotel</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Park Hyatt Milan</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Portrait Milano - Lungarno Collection</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte House, Milan</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Straf, Milan, a Member Of Design Hotels</td><td>Milan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Carlton, Milan, a Rocco Forte Hotel</td><td>Milan</td><td>—</td></tr>
</tbody></table>

#### Montaione

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castelfalfi</td><td>Montaione</td><td>—</td></tr>
</tbody></table>

#### Montalcino

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castello Banfi - Il Borgo - Relais et Chateaux</td><td>Montalcino</td><td>—</td></tr>
</tbody></table>

#### Noto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il San Corrado di Noto Luxury Resort</td><td>Noto</td><td>—</td></tr>
</tbody></table>

#### Palermo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Villa Igiea</td><td>Palermo</td><td>—</td></tr>
</tbody></table>

#### Pinzolo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Lefay Resort &amp; SPA Dolomiti</td><td>Pinzolo</td><td>—</td></tr>
</tbody></table>

#### Porto Ercole

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>La Roqqa</td><td>Porto Ercole</td><td>—</td></tr>
</tbody></table>

#### Portofino

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Splendido Mare, A Belmond Hotel, Portofino</td><td>Portofino</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Splendido, A Belmond Hotel, Portofino</td><td>Portofino</td><td>—</td></tr>
</tbody></table>

#### Radda in Chianti

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Pieve Aldina</td><td>Radda in Chianti</td><td>—</td></tr>
</tbody></table>

#### Rome

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Anantara Palazzo Naiadi Rome Hotel - A Leading Hotel of the World</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Baglioni Hotel Regina - The Leading Hotels of the World</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Bulgari Hotel Roma</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Monti Roma</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Corinthia Rome</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Eden - Dorchester Collection</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Maalot Roma</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Splendide Royal - The Leading Hotels of the World</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>InterContinental Rome Ambasciatori Palace</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>J.K. Place Roma</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Ripetta</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Portrait Roma</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Hotel de la Ville</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Hotel De Russie</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Six Senses Rome</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Sofitel Roma Villa Borghese</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Rome EDITION</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The St. Regis Rome</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Agrippina a Gran Melia Hotel</td><td>Rome</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>W Rome</td><td>Rome</td><td>—</td></tr>
</tbody></table>

#### Saturnia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Terme di Saturnia Natural Spa &amp; Golf Resort</td><td>Saturnia</td><td>—</td></tr>
</tbody></table>

#### Sciacca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Private Villas</td><td>Sciacca</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Verdura Resort</td><td>Sciacca</td><td>—</td></tr>
</tbody></table>

#### Siena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo San Felice Resort</td><td>Siena</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castello di Casole, A Belmond Hotel, Tuscany</td><td>Siena</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Continental Siena – Starhotels Collezione</td><td>Siena</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Le Fontanelle</td><td>Siena</td><td>—</td></tr>
</tbody></table>

#### Sorrento

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Excelsior Vittoria</td><td>Sorrento</td><td>—</td></tr>
</tbody></table>

#### Taormina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Timeo, A Belmond Hotel, Taormina</td><td>Taormina</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Mazzaro&#x27; Sea Palace - VRetreats</td><td>Taormina</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>San Domenico Palace, Taormina, A Four Seasons Hotel</td><td>Taormina</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Ashbee Hotel</td><td>Taormina</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Sant&#x27;Andrea, A Belmond Hotel, Taromina Mare</td><td>Taormina</td><td>—</td></tr>
</tbody></table>

#### Val Gardena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Gardena Grödnerhof Hotel &amp; Spa</td><td>Val Gardena</td><td>—</td></tr>
</tbody></table>

#### Venice

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Baglioni Hotel Luna - The Leading Hotels of the World</td><td>Venice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Ca&#x27; di Dio</td><td>Venice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Cipriani, A Belmond Hotel, Venice</td><td>Venice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Londra Palace Venezia</td><td>Venice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Radisson Collection Palazzo Nani, Venice</td><td>Venice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Gritti Palace, a Luxury Collection Hotel, Venice</td><td>Venice</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The St. Regis Venice</td><td>Venice</td><td>—</td></tr>
</tbody></table>

### Malta

#### Malta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Malta"><td>Iniala Valletta</td><td>Malta</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Malta"><td>InterContinental Malta by IHG</td><td>Malta</td><td>—</td></tr>
</tbody></table>

### Monaco

#### Monaco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Fairmont Monte Carlo</td><td>Monaco</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Hotel de Paris Monte-Carlo</td><td>Monaco</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Hotel Hermitage Monte-Carlo</td><td>Monaco</td><td>—</td></tr>
</tbody></table>

### Montenegro

#### Bay of Kotor

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>One&amp;Only Portonovi</td><td>Bay of Kotor</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>The Chedi Lustica Bay</td><td>Bay of Kotor</td><td>—</td></tr>
</tbody></table>

### Netherlands

#### Amsterdam

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Anantara Grand Hotel Krasnapolsky Amsterdam</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Andaz Amsterdam, Prinsengracht, by Hyatt</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>De L&#x27;Europe Amsterdam</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>InterContinental Amstel Amsterdam by IHG</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Kimpton De Witt Amsterdam by IHG</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Mandarin Oriental Conservatorium, Amsterdam</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Pillows Grand Boutique Hotel Maurits at the Park</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Pulitzer Amsterdam</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Sofitel Legend The Grand Amsterdam</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>The Dylan Amsterdam</td><td>Amsterdam</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Tivoli Doelen Amsterdam Hotel</td><td>Amsterdam</td><td>—</td></tr>
</tbody></table>

### Norway

#### Oslo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>Sommerro</td><td>Oslo</td><td>—</td></tr>
</tbody></table>

### Poland

#### Warsaw

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Poland"><td>Nobu Hotel Warsaw</td><td>Warsaw</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Poland"><td>Raffles Europejski Warsaw</td><td>Warsaw</td><td>—</td></tr>
</tbody></table>

### Portugal

#### Albufeira

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Kimpton Atlântico Algarve by IHG</td><td>Albufeira</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Pine Cliffs Ocean Suites, a Luxury Collection Resort &amp; Spa</td><td>Albufeira</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>W Algarve</td><td>Albufeira</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>W Residences Algarve</td><td>Albufeira</td><td>—</td></tr>
</tbody></table>

#### Azores

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Furnas</td><td>Azores</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Ponta Delgada</td><td>Azores</td><td>—</td></tr>
</tbody></table>

#### Beja

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Herdade da Malhadinha Nova</td><td>Beja</td><td>—</td></tr>
</tbody></table>

#### Castro Marim

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Praia Verde</td><td>Castro Marim</td><td>—</td></tr>
</tbody></table>

#### Douro Valley

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Douro</td><td>Douro Valley</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Six Senses Douro Valley</td><td>Douro Valley</td><td>—</td></tr>
</tbody></table>

#### Lisbon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Andaz Lisbon</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Bairro Alto Hotel - The Leading Hotels of the World</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Convent Square Lisbon, Vignette Collection by IHG</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Corinthia Lisbon</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Four Seasons Hotel Ritz Lisbon</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>InterContinental Lisbon by IHG</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The One Palácio da Anunciada</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Tivoli Avenida Liberdade Lisboa – A Leading hotel of the world</td><td>Lisbon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Valverde Lisboa Hotel &amp; Garden</td><td>Lisbon</td><td>—</td></tr>
</tbody></table>

#### Loulé

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Viceroy at Ombria Algarve</td><td>Loulé</td><td>—</td></tr>
</tbody></table>

#### Madeira

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Reids Palace, A Belmond Hotel, Madeira</td><td>Madeira</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Savoy Palace</td><td>Madeira</td><td>—</td></tr>
</tbody></table>

#### Melides

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Vermelho Melides - Relais &amp; Châteaux</td><td>Melides</td><td>—</td></tr>
</tbody></table>

#### Montemor-o-Novo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>L&#x27;And Vineyards</td><td>Montemor-o-Novo</td><td>—</td></tr>
</tbody></table>

#### Olhão

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Vila Monte</td><td>Olhão</td><td>—</td></tr>
</tbody></table>

#### Portimão

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Bela Vista Hotel &amp; SPA - Relais &amp; Châteaux</td><td>Portimão</td><td>—</td></tr>
</tbody></table>

#### Porto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Casa da Companhia Hotel &amp; Spa, Vignette Collection by IHG</td><td>Porto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>InterContinental Porto-Palacio das Cardosas</td><td>Porto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The Largo</td><td>Porto</td><td>—</td></tr>
</tbody></table>

#### Sintra

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Penha Longa Resort</td><td>Sintra</td><td>—</td></tr>
</tbody></table>

### Romania

#### Bucharest

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Romania"><td>Corinthia Grand Hotel du Boulevard Bucharest</td><td>Bucharest</td><td>—</td></tr>
</tbody></table>

### Spain

#### Arta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Es Racó d’Artà, a Member of Design Hotels™</td><td>Arta</td><td>—</td></tr>
</tbody></table>

#### Banyalbufar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Son Bunyola Hotel</td><td>Banyalbufar</td><td>—</td></tr>
</tbody></table>

#### Barcelona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Almanac Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Grand Hyatt Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Arts Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel El Palace Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Neri Relais &amp; Chateaux</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>InterContinental Barcelona by IHG</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Kimpton Vividora Hotel by IHG</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Majestic Hotel &amp; Spa Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Serras Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Barcelona EDITION</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The One Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>W Barcelona</td><td>Barcelona</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>WITTMORE HOTEL - Adults Only</td><td>Barcelona</td><td>—</td></tr>
</tbody></table>

#### Bilbao

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Radisson Collection Bilbao</td><td>Bilbao</td><td>—</td></tr>
</tbody></table>

#### Calvia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel de Mar a Gran Melia Hotel</td><td>Calvia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Kimpton Aysla Mallorca by IHG</td><td>Calvia</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The St. Regis Mardavall Mallorca Resort</td><td>Calvia</td><td>—</td></tr>
</tbody></table>

#### Canyamel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Cap Vermell Grand Hotel</td><td>Canyamel</td><td>—</td></tr>
</tbody></table>

#### Casares

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Finca Cortesin Hotel Golf &amp; Spa</td><td>Casares</td><td>—</td></tr>
</tbody></table>

#### Córdoba

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Palacio del Bailio</td><td>Córdoba</td><td>—</td></tr>
</tbody></table>

#### Deia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>La Residencia, A Belmond Hotel, Mallorca</td><td>Deia</td><td>—</td></tr>
</tbody></table>

#### Elciego

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Marqués de Riscal, a Luxury Collection Hotel, Elciego</td><td>Elciego</td><td>—</td></tr>
</tbody></table>

#### Granada

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Seda Club Hotel – Small Luxury Hotel</td><td>Granada</td><td>—</td></tr>
</tbody></table>

#### Ibiza

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>BLESS Ibiza Cala Nova</td><td>Ibiza</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Ibiza</td><td>Ibiza</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Mondrian Ibiza</td><td>Ibiza</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel Ibiza Bay</td><td>Ibiza</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Petunia Ibiza, a Beaumier Hotel</td><td>Ibiza</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Six Senses Ibiza</td><td>Ibiza</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Standard, Ibiza</td><td>Ibiza</td><td>—</td></tr>
</tbody></table>

#### Madrid

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Bless Hotel Madrid</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Casa de las Artes, The Melia Collection</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Four Seasons Hotel Madrid</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Gran Hotel Inglés - The Leading Hotels of the World</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Fenix, a Gran Meliá Hotel</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>InterContinental Madrid by IHG</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Palacio de los Duques Gran Meliá - The Leading Hotels of the World</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Santo Mauro, a Luxury Collection Hotel</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Madrid EDITION</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Palace, a Luxury Collection Hotel, Madrid</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Principal Madrid, Small Luxury Hotels</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Thompson Madrid, by Hyatt</td><td>Madrid</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>URSO Hotel &amp; Spa</td><td>Madrid</td><td>—</td></tr>
</tbody></table>

#### Málaga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Palacio Solecio, a Small Luxury Hotel of the World</td><td>Málaga</td><td>—</td></tr>
</tbody></table>

#### Marbella

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Kimpton Los Monteros Marbella</td><td>Marbella</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Marbella Club Hotel Golf Resort &amp; Spa</td><td>Marbella</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel Marbella</td><td>Marbella</td><td>—</td></tr>
</tbody></table>

#### Menorca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Villa Le Blanc, a Gran Meliá Hotel</td><td>Menorca</td><td>—</td></tr>
</tbody></table>

#### Mijas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>La Zambra Resort Mijas - Marbella The Unbound Collection By Hyatt</td><td>Mijas</td><td>—</td></tr>
</tbody></table>

#### Montuïri, Mallorca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Finca Serena, Mallorca</td><td>Montuïri, Mallorca</td><td>—</td></tr>
</tbody></table>

#### Palma de Mallorca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobis Hotel Palma</td><td>Palma de Mallorca</td><td>—</td></tr>
</tbody></table>

#### Pollença

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Four Seasons Resort Mallorca at Formentor</td><td>Pollença</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Lodge Mallorca</td><td>Pollença</td><td>—</td></tr>
</tbody></table>

#### San Sebastián

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Akelarre</td><td>San Sebastián</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Maria Cristina, a Luxury Collection Hotel</td><td>San Sebastián</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel San Sebastián</td><td>San Sebastián</td><td>—</td></tr>
</tbody></table>

#### Sant Adria de Besos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>SLS Barcelona</td><td>Sant Adria de Besos</td><td>—</td></tr>
</tbody></table>

#### Seville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Las Casas del Rey de Baeza, a Member of Design Hotels</td><td>Seville</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Alfonso XIII, a Luxury Collection Hotel, Seville</td><td>Seville</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Colon, a Gran Melia Hotel</td><td>Seville</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Radisson Collection, Magdalena Plaza Sevilla</td><td>Seville</td><td>—</td></tr>
</tbody></table>

#### Sóller

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Jumeirah Mallorca</td><td>Sóller</td><td>—</td></tr>
</tbody></table>

#### Sotogrande

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Fairmont La Hacienda Costa del Sol</td><td>Sotogrande</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>SO/ Sotogrande Spa and Golf Resort Hotel Costa del Sol</td><td>Sotogrande</td><td>—</td></tr>
</tbody></table>

#### Tenerife

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Ritz-Carlton Tenerife, Abama</td><td>Tenerife</td><td>—</td></tr>
</tbody></table>

### Sweden

#### Stockholm

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>At Six</td><td>Stockholm</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Grand Hôtel Stockholm</td><td>Stockholm</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Hotel Skeppsholmen, Stockholm, a Member of Design Hotels</td><td>Stockholm</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Nobis Hotel Stockholm</td><td>Stockholm</td><td>—</td></tr>
</tbody></table>

### Switzerland

#### Andermatt

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Radisson Blu Hotel Reussen Andermatt</td><td>Andermatt</td><td>—</td></tr>
</tbody></table>

#### Arosa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Tschuggen Grand Hotel</td><td>Arosa</td><td>—</td></tr>
</tbody></table>

#### Ascona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Eden Roc</td><td>Ascona</td><td>—</td></tr>
</tbody></table>

#### Crans-Montana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Crans Ambassador</td><td>Crans-Montana</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Six Senses Crans-Montana</td><td>Crans-Montana</td><td>—</td></tr>
</tbody></table>

#### Engelberg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Kempinski Palace Engelberg</td><td>Engelberg</td><td>—</td></tr>
</tbody></table>

#### Geneva

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Four Seasons Hotel des Bergues Geneva</td><td>Geneva</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel D&#x27;Angleterre Geneva</td><td>Geneva</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>La Reserve Geneve - Hotel &amp; Spa</td><td>Geneva</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Ritz-Carlton Hotel de la Paix, Geneva</td><td>Geneva</td><td>—</td></tr>
</tbody></table>

#### Gstaad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Alpina Gstaad</td><td>Gstaad</td><td>—</td></tr>
</tbody></table>

#### Lugano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The View Lugano</td><td>Lugano</td><td>—</td></tr>
</tbody></table>

#### St. Moritz

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Carlton Hotel St Moritz</td><td>St. Moritz</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Grand Hotel des Bains Kempinski</td><td>St. Moritz</td><td>—</td></tr>
</tbody></table>

#### Thalwil (Zurich)

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Alex Lake Zürich</td><td>Thalwil (Zurich)</td><td>—</td></tr>
</tbody></table>

#### Verbier

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>W Verbier</td><td>Verbier</td><td>—</td></tr>
</tbody></table>

#### Zermatt

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Mont Cervin Palace</td><td>Zermatt</td><td>—</td></tr>
</tbody></table>

#### Zürich

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>La Réserve Eden au Lac Zurich</td><td>Zürich</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Park Hyatt Zurich</td><td>Zürich</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Dolder Grand</td><td>Zürich</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Widder Hotel</td><td>Zürich</td><td>—</td></tr>
</tbody></table>

### Türkiye

#### Ankara

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Intercontinental Grand Ankara by IHG</td><td>Ankara</td><td>—</td></tr>
</tbody></table>

#### Bodrum

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Six Senses Kaplankaya</td><td>Bodrum</td><td>—</td></tr>
</tbody></table>

#### Cappadocia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Ariana Sustainable Luxury Lodge - Special Class</td><td>Cappadocia</td><td>—</td></tr>
</tbody></table>

#### Istanbul

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Aliée Istanbul - A Paris Society Collection Hotel</td><td>Istanbul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Four Seasons Hotel Istanbul at Sultanahmet - Special Class</td><td>Istanbul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Four Seasons Hotel Istanbul at the Bosphorus</td><td>Istanbul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Raffles Istanbul</td><td>Istanbul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>The Bank Hotel Istanbul</td><td>Istanbul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>The Peninsula Istanbul</td><td>Istanbul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>The Ritz-Carlton, Istanbul</td><td>Istanbul</td><td>—</td></tr>
</tbody></table>

### United Kingdom

#### Ascot

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Coworth Park - Dorchester Collection</td><td>Ascot</td><td>—</td></tr>
</tbody></table>

#### Bath

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Royal Crescent Hotel &amp; Spa</td><td>Bath</td><td>—</td></tr>
</tbody></table>

#### Edinburgh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>100 Princes Street</td><td>Edinburgh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>InterContinental Edinburgh The George by IHG</td><td>Edinburgh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Kimpton Charlotte Square by IHG</td><td>Edinburgh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Balmoral Hotel</td><td>Edinburgh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Gleneagles Townhouse</td><td>Edinburgh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Virgin Hotels Edinburgh</td><td>Edinburgh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>W Edinburgh</td><td>Edinburgh</td><td>—</td></tr>
</tbody></table>

#### Egham

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Fairmont Windsor Park</td><td>Egham</td><td>—</td></tr>
</tbody></table>

#### Girvan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Glenapp Castle</td><td>Girvan</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Trump Turnberry</td><td>Girvan</td><td>—</td></tr>
</tbody></table>

#### Glasgow

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Kimpton Blythswood Square Hotel</td><td>Glasgow</td><td>—</td></tr>
</tbody></table>

#### Gleneagles

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Gleneagles Hotel</td><td>Gleneagles</td><td>—</td></tr>
</tbody></table>

#### Hampshire

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Four Seasons Hotel Hampshire</td><td>Hampshire</td><td>—</td></tr>
</tbody></table>

#### London

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>1 Hotel Mayfair</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>11 Cadogan Gardens and The Apartments</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>45 Park Lane - Dorchester Collection</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Aethos London Shoreditch</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Brown&#x27;s Hotel, a Rocco Forte Hotel</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Bulgari Hotel London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Claridge&#x27;s</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>COMO Metropolitan London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Corinthia London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Dorset Square Hotel, Firmdale Hotels</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Four Seasons Hotel London at Park Lane</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Four Seasons Hotel London at Tower Bridge</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Grosvenor House Suites</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Haymarket Hotel, Firmdale Hotels</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Hotel Cafe Royal, London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>InterContinental London Park Lane by IHG</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Kimpton Fitzroy London by IHG</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>NoMad London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>One Aldwych</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Park Hyatt London River Thames</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Raffles London at The OWO</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Shangri-La The Shard, London</td><td>London</td><td><a href="https://www.youtube.com/watch?v=qTc6jlWKKzU">Video</a></td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Six Senses London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>St Martins Lane London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Berkeley, Maybourne</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Cadogan, A Belmond Hotel, London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Chelsea Townhouse</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Connaught</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Dorchester</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Emory</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Lanesborough, Oetker Hotels</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Langham, London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The London EDITION</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Londoner Hotel</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Marylebone Hotel</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Milestone Hotel &amp; Residences</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Ned</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Peninsula London</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Savoy, A Fairmont Managed Hotel</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Soho Hotel, Firmdale Hotels</td><td>London</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Standard, London</td><td>London</td><td>—</td></tr>
</tbody></table>

#### Maidenhead

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Cliveden House</td><td>Maidenhead</td><td>—</td></tr>
</tbody></table>

#### New Forest

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Chewton Glen Hotel &amp; Spa</td><td>New Forest</td><td>—</td></tr>
</tbody></table>

#### Oxford

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Estelle Manor</td><td>Oxford</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Le Manoir aux Quat&#x27;Saisons</td><td>Oxford</td><td>—</td></tr>
</tbody></table>

#### Slough

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Langley, a Luxury Collection Hotel, Buckinghamshire</td><td>Slough</td><td>—</td></tr>
</tbody></table>

## Africa

### Botswana

#### Okavango Delta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Botswana"><td>Belmond Safaris</td><td>Okavango Delta</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Botswana"><td>Xigera Safari Lodge</td><td>Okavango Delta</td><td>—</td></tr>
</tbody></table>

### Egypt

#### Alexandria

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Hotel Alexandria at San Stefano</td><td>Alexandria</td><td>—</td></tr>
</tbody></table>

#### Cairo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Hotel Cairo at First Residence</td><td>Cairo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Hotel Cairo at Nile Plaza</td><td>Cairo</td><td>—</td></tr>
</tbody></table>

#### Sharm El Sheikh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Resort Sharm EL Sheikh</td><td>Sharm El Sheikh</td><td>—</td></tr>
</tbody></table>

### Mauritius

#### Mauritius

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>Four Seasons Mauritius at Anahita</td><td>Mauritius</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>LUX* Grand Baie</td><td>Mauritius</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>One&amp;Only Le Saint Géran</td><td>Mauritius</td><td>—</td></tr>
</tbody></table>

### Morocco

#### Casablanca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Four Seasons Hotel Casablanca</td><td>Casablanca</td><td>—</td></tr>
</tbody></table>

#### Marrakech

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Four Seasons Resort Marrakech</td><td>Marrakech</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Kasbah Tamadot</td><td>Marrakech</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>La Sultana Marrakech</td><td>Marrakech</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Nobu Hotel Marrakech</td><td>Marrakech</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Park Hyatt Marrakech</td><td>Marrakech</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Royal Mansour Marrakech</td><td>Marrakech</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>The Oberoi Marrakech</td><td>Marrakech</td><td>—</td></tr>
</tbody></table>

#### Rabat

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Four Seasons Hotel Rabat at Kasr Al Bahr</td><td>Rabat</td><td>—</td></tr>
</tbody></table>

### Rwanda

#### Nyungwe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Rwanda"><td>Nyungwe Tea Forest Resort</td><td>Nyungwe</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Rwanda"><td>One&amp;Only Nyungwe House</td><td>Nyungwe</td><td>—</td></tr>
</tbody></table>

### Seychelles

#### Seychelles

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Four Seasons Resort Seychelles</td><td>Seychelles</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Four Seasons Resort Seychelles at Desroches Island</td><td>Seychelles</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Six Senses Zil Pasyon Seychelles</td><td>Seychelles</td><td>—</td></tr>
</tbody></table>

### South Africa

#### Cape Town

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Cape Grace, A Fairmont Managed Hotel</td><td>Cape Town</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Ellerman House</td><td>Cape Town</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Mount Nelson, A Belmond Hotel, Cape Town</td><td>Cape Town</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>One&amp;Only Cape Town</td><td>Cape Town</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>The Twelve Apostles Hotel and Spa</td><td>Cape Town</td><td>—</td></tr>
</tbody></table>

#### Johannesburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Four Seasons Hotel The Westcliff, Johannesburg</td><td>Johannesburg</td><td>—</td></tr>
</tbody></table>

### Tunisia

#### Tunis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tunisia"><td>Four Seasons Hotel Tunis</td><td>Tunis</td><td>—</td></tr>
</tbody></table>

## Middle East

### Azerbaijan

#### Baku

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Azerbaijan"><td>Four Seasons Hotel Baku</td><td>Baku</td><td>—</td></tr>
</tbody></table>

### Bahrain

#### Manama

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Bahrain"><td>Four Seasons Hotel Bahrain Bay</td><td>Manama</td><td>—</td></tr>
</tbody></table>

### Israel

#### Jerusalem

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>King David, Jerusalem</td><td>Jerusalem</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>Mamilla Hotel</td><td>Jerusalem</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>The David Citadel Jerusalem</td><td>Jerusalem</td><td>—</td></tr>
</tbody></table>

#### Tel Aviv

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>InterContinental David Tel Aviv by IHG</td><td>Tel Aviv</td><td>—</td></tr>
</tbody></table>

### Jordan

#### Amman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Jordan"><td>Four Seasons Hotel Amman</td><td>Amman</td><td>—</td></tr>
</tbody></table>

### Kuwait

#### Kuwait City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Kuwait"><td>Four Seasons Hotel Kuwait at Burj Alshaya</td><td>Kuwait City</td><td>—</td></tr>
</tbody></table>

### Qatar

#### Doha

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Qatar"><td>Four Seasons Hotel Doha</td><td>Doha</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Qatar"><td>Four Seasons Resort And Residences At The Pearl - Qatar</td><td>Doha</td><td>—</td></tr>
</tbody></table>

### Saudi Arabia

#### Red Sea

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia"><td>Six Senses Southern Dunes, The Red Sea</td><td>Red Sea</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia"><td>The St. Regis Red Sea Resort</td><td>Red Sea</td><td>—</td></tr>
</tbody></table>

#### Riyadh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia"><td>Four Seasons Hotel Riyadh</td><td>Riyadh</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Saudi Arabia"><td>Kimpton KAFD Riyadh by IHG</td><td>Riyadh</td><td>—</td></tr>
</tbody></table>

### United Arab Emirates

#### Abu Dhabi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Four Seasons Hotel Abu Dhabi at Al Maryah Island</td><td>Abu Dhabi</td><td>—</td></tr>
</tbody></table>

#### Dubai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Atlantis The Royal</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Bulgari Resort Dubai</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Four Seasons Hotel Dubai International Financial Centre</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Four Seasons Resort Dubai at Jumeirah Beach</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>InterContinental Residences Dubai Business Bay by IHG</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Jumeirah Al Naseem Dubai</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Jumeirah Burj Al Arab Dubai</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Jumeirah Dar Al Masyaf</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Jumeirah Marsa Al Arab</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>One&amp;Only The Palm</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>SLS Dubai Hotel &amp; Residences</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>SO/ Uptown Dubai</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Taj Dubai</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>The Lana - Dorchester Collection</td><td>Dubai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>The Ritz-Carlton, Dubai</td><td>Dubai</td><td>—</td></tr>
</tbody></table>

## Asia

### Cambodia

#### Krabey Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Six Senses Krabey Island</td><td>Krabey Island</td><td>—</td></tr>
</tbody></table>

#### Siem Reap

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Raffles Grand Hotel d&#x27;Angkor</td><td>Siem Reap</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Shinta Mani Angkor</td><td>Siem Reap</td><td>—</td></tr>
</tbody></table>

### China

#### Beijing

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Bulgari Hotel Beijing</td><td>Beijing</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Beijing</td><td>Beijing</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Peninsula Beijing</td><td>Beijing</td><td>—</td></tr>
</tbody></table>

#### Hangzhou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Hangzhou At Hangzhou Centre</td><td>Hangzhou</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Hangzhou at West Lake</td><td>Hangzhou</td><td>—</td></tr>
</tbody></table>

#### Jiuzhaigou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Rissai Valley, a Ritz-Carlton Reserve</td><td>Jiuzhaigou</td><td>—</td></tr>
</tbody></table>

#### Shanghai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Bulgari Hotel Shanghai</td><td>Shanghai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Kimpton Qiantan Shanghai by IHG</td><td>Shanghai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Peninsula Shanghai</td><td>Shanghai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Shanghai EDITION</td><td>Shanghai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Upper House Shanghai</td><td>Shanghai</td><td>—</td></tr>
</tbody></table>

#### Shenzhen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Shenzhen</td><td>Shenzhen</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Langham, Shenzhen</td><td>Shenzhen</td><td>—</td></tr>
</tbody></table>

#### Suzhou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Suzhou</td><td>Suzhou</td><td>—</td></tr>
</tbody></table>

#### Tianjin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Tianjin</td><td>Tianjin</td><td>—</td></tr>
</tbody></table>

#### Zhengzhou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Intercontinental Zhengzhou by IHG</td><td>Zhengzhou</td><td>—</td></tr>
</tbody></table>

### Hong Kong SAR China

#### Hong Kong

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>Four Seasons Hotel Hong Kong</td><td>Hong Kong</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>Island Shangri-La, Hong Kong</td><td>Hong Kong</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>Mondrian Hong Kong</td><td>Hong Kong</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>The Langham, Hong Kong</td><td>Hong Kong</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>Upper House Hong Kong</td><td>Hong Kong</td><td>—</td></tr>
</tbody></table>

#### Kowloon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>Kerry Hotel, Hong Kong</td><td>Kowloon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>Regent Hong Kong</td><td>Kowloon</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong SAR China"><td>The Peninsula Hong Kong</td><td>Kowloon</td><td>—</td></tr>
</tbody></table>

### India

#### Bengaluru

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Four Seasons Hotel Bengaluru at Embassy One</td><td>Bengaluru</td><td>—</td></tr>
</tbody></table>

#### Dehradun

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Six Senses Vana - A Wellness Retreat</td><td>Dehradun</td><td>—</td></tr>
</tbody></table>

#### Jaipur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Raffles Jaipur</td><td>Jaipur</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi Rajvilas</td><td>Jaipur</td><td>—</td></tr>
</tbody></table>

#### Mumbai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Four Seasons Hotel Mumbai</td><td>Mumbai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Taj Mahal Palace Mumbai</td><td>Mumbai</td><td>—</td></tr>
</tbody></table>

#### New Delhi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Mahal, New Delhi</td><td>New Delhi</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Leela Palace New Delhi</td><td>New Delhi</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi, New Delhi</td><td>New Delhi</td><td>—</td></tr>
</tbody></table>

#### Ranthambore

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Six Senses Fort Barwara</td><td>Ranthambore</td><td>—</td></tr>
</tbody></table>

#### Udaipur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Raffles Udaipur</td><td>Udaipur</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi Udaivilas</td><td>Udaipur</td><td>—</td></tr>
</tbody></table>

### Indonesia

#### Bali

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Andaz Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Bvlgari Resort Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>COMO Canggu</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>COMO Shambhala Estate</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>COMO Uma Canggu</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Four Seasons Resort Bali at Jimbaran Bay</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Four Seasons Resort Bali at Sayan</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Jimbaran Puri, A Belmond Hotel, Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Jumeirah Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Mandapa, a Ritz-Carlton Reserve</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Raffles Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Regent Bali Canggu</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Six Senses Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Soori Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Apurva Kempinski Bali</td><td>Bali</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The St. Regis Bali Resort</td><td>Bali</td><td>—</td></tr>
</tbody></table>

#### Jakarta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Four Seasons Hotel Jakarta</td><td>Jakarta</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Langham, Jakarta</td><td>Jakarta</td><td>—</td></tr>
</tbody></table>

#### Sumba

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>NIHI Sumba</td><td>Sumba</td><td>—</td></tr>
</tbody></table>

### Japan

#### Kyoto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Ace Hotel Kyoto</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Banyan Tree Higashiyama Kyoto</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Kyoto</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Garrya Nijo Castle Kyoto</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Park Hyatt Kyoto</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Six Senses Kyoto</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Sowaka</td><td>Kyoto</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Suiran, A Luxury Collection Hotel, Kyoto</td><td>Kyoto</td><td><a href="https://visitkarma.com/p/suiran-kyoto-arashiyama-review-marriott-luxury-collection-onsen-ryokan-stay/">Blog</a> · <a href="https://www.youtube.com/watch?v=RJSN7wgPO40">Video</a></td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Kyoto</td><td>Kyoto</td><td>—</td></tr>
</tbody></table>

#### Miyakojima

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>IRAPH SUI, a Luxury Collection Hotel, Miyako Okinawa</td><td>Miyakojima</td><td>—</td></tr>
</tbody></table>

#### Nikko

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Nikko</td><td>Nikko</td><td>—</td></tr>
</tbody></table>

#### Niseko

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Park Hyatt Niseko Hanazono</td><td>Niseko</td><td>—</td></tr>
</tbody></table>

#### Osaka

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Osaka</td><td>Osaka</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>InterContinental Osaka by IHG</td><td>Osaka</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Osaka</td><td>Osaka</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>W Osaka</td><td>Osaka</td><td>—</td></tr>
</tbody></table>

#### Tokyo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Andaz Tokyo Toranomon Hills</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Bellustar Tokyo, a Pan Pacific Hotel</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Bulgari Hotel Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Fairmont Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Tokyo at Marunouchi</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Tokyo at Otemachi</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Grand Hyatt Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Kimpton Shinjuku Tokyo by IHG</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Palace Hotel Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Park Hyatt Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Shangri-La Tokyo</td><td>Tokyo</td><td><a href="https://www.youtube.com/watch?v=0-9yoNhmLtk">Video</a></td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Okura Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Peninsula Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Prince Gallery Tokyo Kioicho, a Luxury Collection Hotel</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Tokyo</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Strings by InterContinental Tokyo by IHG</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Tokyo EDITION, Ginza</td><td>Tokyo</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Tokyo EDITION, Toranomon</td><td>Tokyo</td><td>—</td></tr>
</tbody></table>

### Macao SAR China

#### Macau

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Macao SAR China"><td>Four Seasons Hotel Macao</td><td>Macau</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Macao SAR China"><td>The Grand Suites at Four Seasons</td><td>Macau</td><td>—</td></tr>
</tbody></table>

### Malaysia

#### Kuala Lumpur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Four Seasons Hotel Kuala Lumpur</td><td>Kuala Lumpur</td><td>—</td></tr>
</tbody></table>

#### Langkawi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Four Seasons Resort Langkawi</td><td>Langkawi</td><td>—</td></tr>
</tbody></table>

### Maldives

#### Maldives

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>COMO Cocoa Island</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Four Seasons Maldives At Kuda Huraa</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Four Seasons Maldives at Landaa Giraavaru</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>InterContinental Maldives Maamunagau Resort by IHG</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>JOALI Maldives</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>LUX* South Ari Atoll</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Naladhu Private Island Maldives Resort</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>One&amp;Only Reethi Rah</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Six Senses Kanuhura</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Six Senses Laamu</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Soneva Fushi</td><td>Maldives</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Taj Exotica Resort &amp; Spa, Maldives</td><td>Maldives</td><td>—</td></tr>
</tbody></table>

### Philippines

#### Boracay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Shangri-La Boracay</td><td>Boracay</td><td>—</td></tr>
</tbody></table>

#### Manila

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Raffles Makati</td><td>Manila</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Shangri-La The Fort, Manila</td><td>Manila</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>The Peninsula Manila</td><td>Manila</td><td>—</td></tr>
</tbody></table>

### Singapore

#### Singapore

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Capella Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>COMO Metropolitan Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Four Seasons Hotel Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>InterContinental Singapore Robertson Quay by IHG</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>JW Marriott Hotel Singapore South Beach</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Marina Bay Sands</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Mondrian Singapore Duxton</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Pan Pacific Orchard</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Pan Pacific Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Raffles Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Fullerton Bay Hotel Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Ritz-Carlton, Millenia Singapore</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The St. Regis Singapore (Newly Renovated)</td><td>Singapore</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Standard, Singapore</td><td>Singapore</td><td>—</td></tr>
</tbody></table>

### South Korea

#### Seoul

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Four Seasons Hotel Seoul</td><td>Seoul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>InterContinental Grand Seoul Parnas</td><td>Seoul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Mondrian Seoul Itaewon</td><td>Seoul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Park Hyatt Seoul</td><td>Seoul</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>The Shilla Seoul</td><td>Seoul</td><td>—</td></tr>
</tbody></table>

### Taiwan

#### Taipei

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Hotel Proverbs Taipei</td><td>Taipei</td><td>—</td></tr>
</tbody></table>

### Thailand

#### Bangkok

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Andaz One Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Capella Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Hotel Bangkok at Chao Phraya River</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Kimpton Maa-Lai Bangkok by IHG</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Park Hyatt Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Sindhorn Kempinski Hotel Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Peninsula Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Ritz-Carlton, Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Siam</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The St. Regis Bangkok</td><td>Bangkok</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Standard, Bangkok Mahanakhon</td><td>Bangkok</td><td>—</td></tr>
</tbody></table>

#### Chiang Mai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Chiang Mai Resort</td><td>Chiang Mai</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Resort Chiang Mai</td><td>Chiang Mai</td><td>—</td></tr>
</tbody></table>

#### Golden Triangle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Tented Camp Golden Triangle</td><td>Golden Triangle</td><td>—</td></tr>
</tbody></table>

#### Khao Lak

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Devasom Khao Lak Beach Resort &amp; Villas</td><td>Khao Lak</td><td>—</td></tr>
</tbody></table>

#### Koh Samui

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Lawana Koh Samui Resort</td><td>Koh Samui</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Banyan Tree Samui</td><td>Koh Samui</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Resort Koh Samui</td><td>Koh Samui</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Kimpton Kitalay Samui by IHG</td><td>Koh Samui</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Ritz-Carlton, Koh Samui</td><td>Koh Samui</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Vana Belle, a Luxury Collection Resort, Koh Samui</td><td>Koh Samui</td><td>—</td></tr>
</tbody></table>

#### Krabi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Banyan Tree Krabi</td><td>Krabi</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Phulay Bay, a Ritz-Carlton Reserve</td><td>Krabi</td><td>—</td></tr>
</tbody></table>

#### Pattaya

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Andaz Pattaya Jomtien Beach</td><td>Pattaya</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Pattaya Resort by IHG</td><td>Pattaya</td><td>—</td></tr>
</tbody></table>

#### Phuket

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Layan Phuket Resort &amp; Layan Residences</td><td>Phuket</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Banyan Tree Phuket</td><td>Phuket</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Dinso Resort &amp; Villas Phuket, Vignette Collection by IHG</td><td>Phuket</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Iniala Beach House</td><td>Phuket</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Phuket Resort by IHG</td><td>Phuket</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Keemala</td><td>Phuket</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Naka Island, a Luxury Collection Resort &amp; Spa, Phuket</td><td>Phuket</td><td>—</td></tr>
</tbody></table>

#### Suratthani

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Rasananda Koh Phangan Villas</td><td>Suratthani</td><td>—</td></tr>
</tbody></table>

### Vietnam

#### Con Dao

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Six Senses Con Dao</td><td>Con Dao</td><td>—</td></tr>
</tbody></table>

#### Ha Long Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>InterContinental Halong Bay Resort by IHG</td><td>Ha Long Bay</td><td>—</td></tr>
</tbody></table>

#### Hanoi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Capella Hanoi</td><td>Hanoi</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Sofitel Legend Metropole Hanoi</td><td>Hanoi</td><td>—</td></tr>
</tbody></table>

#### Hoi An

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Four Seasons Resort The Nam Hai, Hoi An, Vietnam</td><td>Hoi An</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Moire Hoi An, Vignette Collection</td><td>Hoi An</td><td>—</td></tr>
</tbody></table>

#### Lang Co

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Banyan Tree Lang Co</td><td>Lang Co</td><td>—</td></tr>
</tbody></table>

#### Ninh Van Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Six Senses Ninh Van Bay</td><td>Ninh Van Bay</td><td>—</td></tr>
</tbody></table>

#### Phu Quoc

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>JW Marriott Phu Quoc Emerald Bay Resort &amp; Spa</td><td>Phu Quoc</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Regent Phu Quoc</td><td>Phu Quoc</td><td>—</td></tr>
</tbody></table>

## Oceania

### Australia

#### Adelaide Hills

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Mount Lofty House &amp; Estate Adelaide Hills - Adults Retreat</td><td>Adelaide Hills</td><td>—</td></tr>
</tbody></table>

#### Brisbane

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>W Brisbane</td><td>Brisbane</td><td>—</td></tr>
</tbody></table>

#### Cairns

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Shangri-La The Marina, Cairns</td><td>Cairns</td><td>—</td></tr>
</tbody></table>

#### Docklands

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>1 Hotel Melbourne</td><td>Docklands</td><td>—</td></tr>
</tbody></table>

#### Gold Coast

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Langham, Gold Coast</td><td>Gold Coast</td><td>—</td></tr>
</tbody></table>

#### Melbourne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Park Hyatt Melbourne</td><td>Melbourne</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sofitel Melbourne On Collins</td><td>Melbourne</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Langham, Melbourne</td><td>Melbourne</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>W Melbourne</td><td>Melbourne</td><td>—</td></tr>
</tbody></table>

#### Perth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>COMO The Treasury</td><td>Perth</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Ritz-Carlton, Perth</td><td>Perth</td><td>—</td></tr>
</tbody></table>

#### Sydney

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Four Seasons Hotel Sydney</td><td>Sydney</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Sydney by IHG</td><td>Sydney</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Kimpton Margot Sydney by IHG</td><td>Sydney</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Shangri-La Sydney</td><td>Sydney</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Langham, Sydney</td><td>Sydney</td><td>—</td></tr>
</tbody></table>

### Fiji

#### Fiji

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>Nanuku Resort, Fiji</td><td>Fiji</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>Six Senses Fiji</td><td>Fiji</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>Sofitel Fiji Resort &amp; Spa Denarau Island</td><td>Fiji</td><td>—</td></tr>
</tbody></table>

### French Polynesia

#### Bora Bora

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Four Seasons Resort Bora Bora</td><td>Bora Bora</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>InterContinental Bora Bora Resort and Thalasso Spa by IHG</td><td>Bora Bora</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Le Bora Bora</td><td>Bora Bora</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>The St. Regis Bora Bora Resort</td><td>Bora Bora</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>The Westin Bora Bora Resort &amp; Spa</td><td>Bora Bora</td><td>—</td></tr>
</tbody></table>

#### Moorea

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Sofitel Kia Ora Moorea Beach Resort</td><td>Moorea</td><td>—</td></tr>
</tbody></table>

#### Tapuamu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Le Taha&#x27;a</td><td>Tapuamu</td><td>—</td></tr>
</tbody></table>

#### Tetiaroa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>The Brando</td><td>Tetiaroa</td><td>—</td></tr>
</tbody></table>

### New Zealand

#### Auckland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Cordis, Auckland</td><td>Auckland</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Hotel Indigo Auckland by IHG</td><td>Auckland</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>InterContinental Auckland</td><td>Auckland</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Park Hyatt Auckland</td><td>Auckland</td><td>—</td></tr>
</tbody></table>

#### Glenorchy

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Blanket Bay</td><td>Glenorchy</td><td>—</td></tr>
</tbody></table>

