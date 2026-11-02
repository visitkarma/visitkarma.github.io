---
title: "American Express Fine Hotels + Resorts and The Hotel Collection: Every Hotel, by Region and Country"
date: 2026-11-02
lastmod: 2026-11-02
slug: "amex-fine-hotels-resorts-hotel-collection-list"
description: "The American Express Fine Hotels + Resorts and The Hotel Collection lists — 3,146 hotels compiled from dated third-party sources, grouped by region, country and city, searchable and filterable — plus how the Amex hotel perks work."
categories: ["Travel Tips"]
tags: [amex, fine-hotels-resorts, hotel-collection, hotel-list]
pinned: true
---

## What these two programs are

American Express has two hotel programs, both booked through Amex Travel:

- **Fine Hotels + Resorts (FHR)** — for Platinum Card and Centurion members. A typical FHR stay includes daily breakfast for two, a $100 property credit, a room upgrade on arrival when available, early check-in and late check-out when available, and noon check-in where offered.
- **The Hotel Collection (THC)** — for Gold Card and other eligible Amex cardholders. Benefits are lighter and vary more by property, typically a $100 property credit and a room upgrade when available.

Perks and eligibility vary by property and by card, so confirm the exact benefits for your hotel and dates in Amex Travel before you book.

## How to use this list

Use the search box to find a hotel, city, or country, or pick a region or country from the menus — the tables filter live, and the count below the menus tells you how many hotels match. Where we have reviewed a hotel ourselves, the **Our review** column links to our blog post and YouTube video for it.

## The list below — and its limits, stated plainly

This is **not** Amex's own list: Amex publishes no complete public list of FHR or THC hotels. It is compiled from two dated third-party sources:

- **FHR: 1,940 hotels**, from AwardTravel's FHR list, stated as last updated **October 18, 2026**. That extraction matches the source's claimed total exactly, so the FHR section is a faithful copy of that snapshot.
- **THC: 1,206 hotels**, from Perkmon's THC list, stated as reviewed **August 20, 2026**. That is **13 short of Perkmon's own claimed 1,219**, and **268 short of AwardHack's October 2026 crawl (1,474 THC)** — so treat the THC section as a substantial partial list, not a complete one. Perkmon also gives no country headings, so every THC country below is inferred from the heading, city, or hotel name.

Combined, the two sections total **3,146 hotels**, at least **254 short of Amex's own 3,400+ headline** for the two programs together. One hotel appears in both programs and is listed twice, once per program, intentionally.

Two more cautions. Seven THC entries in the source link to Chase's travel site rather than Amex's, which is suspicious: Limelight Mammoth, SLS Beverly Hills, Hotel Polaris, Limelight Boulder, 21c Museum Hotel Louisville, W Fort Lauderdale, and Hotel Saint Augustine — verify those seven in Amex Travel before treating them as THC hotels. And seven THC entries could not be assigned a country with confidence; they sit under **Uncertain** at the end of the list, with their best-guess locations noted in the source notes.

Hotel membership changes through the year — hotels join and leave — so confirm a hotel is still in FHR or THC in Amex Travel before you plan around it. This page is a reference list, not a booking site, and we are not paid by Amex or any hotel on it.

A note for East Africa travellers: unlike The Edit, which has no hotels in Kenya or Tanzania, this Amex list does — including JW Marriott Masai Mara Lodge and Hemingways Nairobi in Kenya, and Four Seasons Safari Lodge Serengeti, Melia Serengeti Lodge, and Park Hyatt Zanzibar in Tanzania. They are in the Africa tables below.

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

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>1 Hotel Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Auberge Saint-Antoine</td><td>Québec City</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Clayoquot Wilderness Lodge, Beckons</td><td>Alberni-Clayoquot C</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Banff Springs</td><td>Banff</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Chateau Lake Louise</td><td>Lake Louise</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Chateau Whistler</td><td>Whistler</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Empress, Victoria</td><td>Victoria</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Le Chateau Frontenac</td><td>Québec City</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Pacific Rim</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Tremblant</td><td>Mont-Tremblant</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Waterfront</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fogo Island Inn</td><td>Joe Batt&#x27;s Arm</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Four Seasons Hotel Montreal</td><td>Montréal</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Four Seasons Hotel Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Four Seasons Resort Whistler</td><td>Whistler</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Hyatt Vancouver Downtown Alberni</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>JW Marriott Parq Vancouver</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Loden Boutique Hotel Vancouver</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Manoir Hovey</td><td>North Hatley</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Muir, a Luxury Collection Hotel, Halifax</td><td>Halifax</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Nobu Hotel Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Pan Pacific Vancouver Pacific Club</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Park Hyatt Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Rosewood Hotel Georgia</td><td>Vancouver</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Shangri-La Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Fairmont Jasper Park Lodge</td><td>Jasper</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Hazelton Hotel Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Ritz-Carlton Montreal</td><td>Montréal</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Ritz-Carlton, Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The St. Regis Toronto</td><td>Toronto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Vogue Hotel Downtown Montreal, Curio Collection by Hilton</td><td>Montréal</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Alberta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Hotel Macdonald</td><td>Edmonton, Alberta</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Dorian, Autograph Collection</td><td>Calgary, Alberta</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### British Columbia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>AZUR Legacy Collection Hotel</td><td>Vancouver, British Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Hotel Vancouver</td><td>Vancouver, British Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Pan Pacific Vancouver</td><td>Vancouver, British Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The DOUGLAS, Autograph Collection Hotels, Vancouver</td><td>Vancouver, British Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Josie Hotel, Autograph Collection</td><td>Rossland, British Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Westin Bayshore, Vancouver</td><td>Vancouver, British Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Wedgewood Hotel and Spa</td><td>Vancouver, British Columbia</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nova Scotia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fox Harbr Resort</td><td>Fox Harbour, Nova Scotia</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ontario

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Ace Hotel Toronto</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Andaz Ottawa Byward Market</td><td>Ottawa, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Bisha, a Luxury Collection Hotel, Toronto</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Canopy by Hilton Toronto - Yorkville</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Chateau Laurier</td><td>Ottawa, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Fairmont Royal York</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Le Germain Hotel Ottawa</td><td>Ottawa, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Le Germain Hotel Toronto Mercer</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>Revery Toronto Downtown, Curio Collection by Hilton</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>SoHo Hotel Toronto</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Drake Hotel</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Omni King Edward Hotel</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>The Yorkville Royal Sonesta Hotel Toronto</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Canada"><td>W Toronto</td><td>Toronto, Ontario</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Mexico

#### Ontario

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>ATELIER Playa Mujeres</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Alila Mayakoba</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Cabo Marques</td><td>Acapulco, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Mayakoba</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Puebla</td><td>Puebla, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Banyan Tree Veya Valle de Guadalupe</td><td>Ensenada, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Cala de Mar Resort &amp; Spa Ixtapa</td><td>Ixtapa, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Casa Polanco</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Casa de Sierra Nevada, A Belmond Hotel, San Miguel de Allende</td><td>San Miguel de Allende, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Chable Maroma</td><td>Punta Maroma, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Chable Yucatan</td><td>Chochola, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Chileno Bay Resort &amp; Residences, Auberge Collection</td><td>Cabo San Lucas, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Conrad Punta de Mita</td><td>Punta de Mita, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Conrad Tulum Riviera Maya</td><td>Tulum, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Esperanza, Auberge Collection</td><td>Cabo San Lucas, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Etereo, Auberge Collection</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Fairmont Heritage Place, Mayakoba</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Hotel Mexico City</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Resort Punta Mita</td><td>Punta de Mita, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Resort Tamarindo, Mexico</td><td>La Huerta, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Four Seasons Resort and Residences Los Cabos at Costa Palmas</td><td>La Ribera, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Boutique Hotel</td><td>San José del Cabo, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Los Cabos</td><td>Cabo San Lucas, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Grand Velas Riviera Nayarit</td><td>Nuevo Vallarta, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hacienda Xcanatun, Angsana Heritage Collection</td><td>Mérida, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Alexander</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Esencia</td><td>Xpu Ha, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Impression Isla Mujeres by Secrets</td><td>Isla Mujeres, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Impression Moxche by Secrets</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>InterContinental Presidente Monterrey</td><td>San Pedro Garza Garcia, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>JW Marriott Mexico City Polanco</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kempinski Hotel Cancun</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>La Casa De La Playa</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Las Alcobas, A Luxury Collection Hotel, Mexico City</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Las Ventanas al Paraiso, A Rosewood Resort</td><td>San Jose del Cabo, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Live Aqua San Miguel de Allende</td><td>San Miguel de Allende, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Maroma, A Belmond Hotel, Riviera Maya</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Montage Los Cabos</td><td>Cabo San Lucas, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>NIZUC Resort &amp; Spa</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Naviva, A Four Seasons Resort, Punta Mita - All Inclusive</td><td>Punta Mita, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Numu Boutique Hotel San Miguel de Allende</td><td>San Miguel de Allende, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>One&amp;Only Mandarina</td><td>Municipio de Compostela, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>One&amp;Only Palmilla</td><td>San Jose del Cabo, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Palmaia - The House of AiA</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Paradero Todos Santos</td><td>Todos Santos, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Park Hyatt Cabo del Sol</td><td>Cabo San Lucas, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Rosewood Mandarina</td><td>El Monteón, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Rosewood Mayakoba</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Rosewood San Miguel de Allende</td><td>San Miguel de Allende, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>SHA Wellness Mexico</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>SLS Cancun</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Siari, a Ritz-Carlton Reserve</td><td>La Peñita de Jaltemba, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Sofitel Mexico City Reforma</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Solaz, a Luxury Collection Resort Los Cabos</td><td>San Jose del Cabo, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Susurros del Corazon, Auberge Collection</td><td>Punta de Mita, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Ritz-Carlton, Mexico City</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Riviera Maya EDITION at Kanai</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St Regis Costa Mujeres Resort Cancun</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St. Regis Kanai Resort, Riviera Maya</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St. Regis Mexico City</td><td>Mexico City, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The St. Regis Punta Mita Resort</td><td>Punta de Mita, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Thompson Zihuatanejo</td><td>Zihuatanejo, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Viceroy Riviera Maya</td><td>Playa del Carmen, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Waldorf Astoria Los Cabos Pedregal</td><td>Cabo San Lucas, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Waldorf Astoria Riviera Maya</td><td>Cancún, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Zadun Los Cabos, a Ritz-Carlton Reserve Residence</td><td>San Jose del Cabo, Ontario</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Zadun Los Cabos, a Ritz-Carlton Reserve</td><td>San Jose del Cabo, Ontario</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Baja California Sur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Corazon Cabo Resort and Spa</td><td>Cabo San Lucas, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Garza Blanca Resort &amp; Spa Los Cabos</td><td>Cabo San Lucas, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel San Cristobal</td><td>Todos Santos, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>JW Marriott Los Cabos Beach Resort &amp; Spa</td><td>San Jose del Cabo, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kimpton Mas Olas Resort And Spa</td><td>El Pescadero, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Le Blanc Spa Resort Los Cabos Adults Only All Inclusive</td><td>San Jose del Cabo, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Nobu Hotel Los Cabos</td><td>Cabo San Lucas, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>The Cape, a Thompson Hotel</td><td>Cabo San Lucas, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Todos Santos Boutique Hotel</td><td>Todos Santos, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Viceroy Los Cabos</td><td>San Jose del Cabo, Baja California Sur</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Villa Santa Cruz</td><td>Todos Santos, Baja California Sur</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Jalisco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hilton Guadalajara Midtown</td><td>Guadalajara, Jalisco</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Mousai Puerto Vallarta</td><td>Puerto Vallarta, Jalisco</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Marriott Puerto Vallarta Resort &amp; Spa</td><td>Puerto Vallarta, Jalisco</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>NH Collection Guadalajara</td><td>Guadalajara, Jalisco</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Mexico City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Andaz Mexico City Condesa</td><td>Mexico City</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hyatt Regency Mexico City</td><td>Mexico City</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kimpton Virgilio Mexico City</td><td>Mexico City</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Mondrian Mexico City Condesa</td><td>Mexico City</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Umbral, Curio Collection by Hilton</td><td>Mexico City</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nayarit

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Secrets Bahia Mita Surf and Spa Resort</td><td>Bahia de Banderas, Nayarit</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>W Punta de Mita</td><td>Punta de Mita, Nayarit</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Oaxaca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>La Valise Mazunte</td><td>Mazunte, Oaxaca</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Quintana Roo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Be Tulum</td><td>Tulum, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Casa Malca</td><td>Tulum, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hilton Tulum Riviera Maya All-Inclusive Resort</td><td>Tulum, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Xcaret Arte</td><td>Playa del Carmen, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Hotel Xcaret Mexico</td><td>Playa del Carmen, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>InterContinental Presidente Cozumel Resort Spa</td><td>Cozumel, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Kimpton Aluna Resort Tulum</td><td>Tulum, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Nomade Holbox</td><td>Holbox, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Our Habitas Bacalar</td><td>Bacalar, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Paradisus Playa del Carmen</td><td>Playa del Carmen, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Secrets Akumal Riviera Maya</td><td>Akumal, Quintana Roo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="Mexico"><td>Secrets Moxche Playa del Carmen</td><td>Playa del Carmen, Quintana Roo</td><td>THC</td><td>—</td></tr>
</tbody></table>

### United States

#### Alabama

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>106 Jefferson Huntsville, Curio Collection by Hilton</td><td>Huntsville, Alabama</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Graduate by Hilton Auburn, AL</td><td>Auburn, Alabama</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Hotel Mountain Brook, Autograph Collection</td><td>Mountain Brook, Alabama</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Laurel Hotel and Spa</td><td>Auburn, Alabama</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Valley Hotel Homewood Birmingham, Curio Collection by Hilton</td><td>Homewood, Alabama</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Arizona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amara Resort &amp; Spa</td><td>Sedona, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ambiente Sedona</td><td>Sedona, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Scottsdale Resort &amp; Bungalows</td><td>Scottsdale, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Arizona Biltmore, LXR Hotels &amp; Resorts</td><td>Phoenix, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>CIVANA Wellness Resort and Spa</td><td>Carefree, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Caesars Republic Scottsdale, a Hilton Hotel</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Scottsdale Old Town</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Tempe Downtown</td><td>Tempe, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canyon Ranch Tucson</td><td>Tucson, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Castle Hot Springs</td><td>Morristown, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Enchantment</td><td>Sedona, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Scottsdale Princess</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Scottsdale at Troon North</td><td>Scottsdale, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Scottsdale Resort</td><td>Scottsdale, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hacienda Del Sol Guest Ranch Resort</td><td>Tucson, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Valley Ho</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Phoenix Desert Ridge Resort and Spa</td><td>Phoenix, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Scottsdale Camelback Inn Resort &amp; Spa</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Palomar Phoenix</td><td>Phoenix, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Miralina Resort &amp; Villas</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Auberge de Sedona</td><td>Sedona, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Ventana Canyon Resort</td><td>Tucson, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mii amo</td><td>Sedona, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Miraval Arizona</td><td>Tucson, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mountain Shadows Resort Scottsdale</td><td>Paradise Valley, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Scottsdale Resort &amp; Spa at Montelucia</td><td>Paradise Valley, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Tempe Hotel</td><td>Tempe, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Tucson National Resort</td><td>Tucson, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Royal Palms Resort and Spa</td><td>Phoenix, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sanctuary Camelback Mountain Resort and Spa</td><td>Paradise Valley, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Senna House Hotel Scottsdale, Curio Collection by Hilton</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sheraton Grand at Wild Horse Pass</td><td>Phoenix, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Canyon Suites at The Phoenician, a Luxury Collection Resort, Scottsdale</td><td>Scottsdale, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Global Ambassador</td><td>Phoenix, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hermosa Inn</td><td>Paradise Valley, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Phoenician, a Luxury Collection Resort, Scottsdale</td><td>Scottsdale, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Dove Mountain</td><td>Marana, Arizona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Scottsdale Resort and Spa, Curio Collection by Hilton</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Kierland Resort &amp; Spa</td><td>Scottsdale, Arizona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Wilde Resort and Spa</td><td>Sedona, Arizona</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Arkansas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Compton Bentonville</td><td>Bentonville, Arkansas</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### California

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel San Francisco</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel West Hollywood</td><td>West Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alila Marea Beach Resort Encinitas</td><td>Encinitas, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alila Napa Valley</td><td>St. Helena, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alila Ventana Big Sur</td><td>Big Sur, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Alma San Diego, A Tribute Portfolio Hotel</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz San Diego</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Argonaut Hotel</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Auberge du Soleil</td><td>Rutherford, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Avalon Beverly Hills</td><td>Beverly Hills, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Balboa Bay Resort</td><td>Newport Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bardessono Hotel &amp; Spa</td><td>Yountville, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Beach Village at The Del, LXR Hotels &amp; Resorts</td><td>Coronado, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Beverly Wilshire, Beverly Hills, A Four Seasons Hotel</td><td>Beverly Hills, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cal-a-Vie Health Spa</td><td>Vista, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cameo Beverly Hills, LXR Hotels &amp; Resorts</td><td>Los Angeles, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cape Rey Carlsbad Beach, a Hilton Resort and Spa</td><td>Carlsbad, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carmel Valley Ranch</td><td>Carmel-By-The-Sea, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carneros Resort and Spa</td><td>Napa, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carte Hotel San Diego Downtown, Curio Collection by Hilton</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Catamaran Resort Hotel and Spa</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cavallo Point Lodge</td><td>Sausalito, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Claremont Resort &amp; Club</td><td>Berkeley, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Colony Palms Hotel and Bungalows</td><td>Palm Springs, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad Los Angeles</td><td>Los Angeles, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>CordeValle</td><td>San Martin, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dawn Ranch</td><td>Guerneville, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Downtown L.A. Proper Hotel</td><td>Los Angeles, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dream Hollywood</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>El Encanto Santa Barbara</td><td>Santa Barbara, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Estancia La Jolla Hotel and Spa</td><td>La Jolla, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Breakers Long Beach</td><td>Long Beach, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Century Plaza Los Angeles at Beverly Hills</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Grand Del Mar</td><td>San Diego, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Miramar Hotel &amp; Bungalows</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont San Francisco</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Sonoma Mission Inn &amp; Spa</td><td>Sonoma, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Farmhouse Inn</td><td>Forestville, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Los Angeles at Beverly Hills</td><td>Los Angeles, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel San Francisco at Embarcadero</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel San Francisco</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Silicon Valley, at East Palo Alto</td><td>East Palo Alto, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Westlake Village, California</td><td>Westlake Village, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Residence Club Aviara</td><td>Carlsbad, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort and Residences Napa Valley</td><td>Calistoga, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Indian Wells Resort and Villas</td><td>Indian Wells, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Guild Hotel, A Marriott Tribute Portfolio Hotel</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hollywood Roosevelt</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bel-Air</td><td>Los Angeles, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Californian</td><td>Santa Barbara, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Casa del Mar</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Healdsburg</td><td>Healdsburg, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel La Jolla, Curio Collection by Hilton</td><td>La Jolla, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel San Luis Obispo</td><td>San Luis Obispo, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Yountville</td><td>Yountville, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel del Coronado</td><td>Coronado, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Huntley Santa Monica Beach Hotel</td><td>Santa Monica, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Huntington Beach Resort and Spa</td><td>Huntington Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency San Francisco Downtown SOMA</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ingleside Estate</td><td>Palm Springs, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn at the Pier Pismo Beach, Curio Collection by Hilton</td><td>Pismo Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Los Angeles Downtown</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental San Diego</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental San Francisco</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Desert Springs Resort &amp; Spa</td><td>Palm Desert, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott L.A. Live</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott San Francisco Union Square</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott, Anaheim Resort</td><td>Anaheim, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Alton Hotel Fisherman&#x27;s Wharf</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Canary Hotel</td><td>Santa Barbara, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Enso</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton La Peer Hotel</td><td>West Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Mirador Pacific Grove</td><td>Pacific Grove, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Rowan Palm Springs Hotel</td><td>Palm Springs, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Sawyer Hotel</td><td>Sacramento, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Shorebreak Resort</td><td>Huntington Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kona Kai San Diego Resort</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Auberge Del Mar</td><td>Del Mar, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Ermitage Beverly Hills</td><td>Beverly Hills, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L&#x27;Horizon Resort &amp; Spa, Hermann Bungalows</td><td>Palm Springs, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>La Bahia Hotel &amp; Spa</td><td>Santa Cruz, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>La Quinta Resort &amp; Club, Curio Collection by Hilton</td><td>La Quinta, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>La Valencia Hotel</td><td>La Jolla, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lido House Hotel, Autograph Collection</td><td>Newport Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Mammoth</td><td>Mammoth Lakes, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Liora Estate</td><td>Healdsburg, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Coronado Bay Resort</td><td>Coronado, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Hollywood Hotel</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>MacArthur Place</td><td>Sonoma, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Malibu Beach Inn</td><td>Malibu, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Margaritaville Hotel San Diego Gaslamp Quarter</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Margaritaville Resort Lake Tahoe</td><td>South Lake Tahoe, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Meadowood Napa Valley</td><td>St. Helena, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mission Pacific Beach Resort</td><td>Oceanside, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Healdsburg</td><td>Healdsburg, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Laguna Beach</td><td>Laguna Beach, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Monterey Plaza Hotel and Spa</td><td>Monterey, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moxy Downtown Los Angeles</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Palo Alto</td><td>Palo Alto, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Oceana Santa Monica, LXR Hotels &amp; Resorts</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ojai Valley Inn</td><td>Ojai, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni La Costa Resort &amp; Spa</td><td>Carlsbad, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Rancho Las Palmas Resort</td><td>Rancho Mirage, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni San Diego Hotel</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Palace Hotel, a Luxury Collection Hotel, San Francisco</td><td>San Francisco, California</td><td>FHR</td><td><a href="https://www.youtube.com/watch?v=USr5hpVl4k4">Video</a></td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Aviara Resort, Golf Club &amp; Spa</td><td>Carlsbad, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Parker Palm Springs</td><td>Palm Springs, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pasea Hotel &amp; Spa</td><td>Huntington Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Newport Beach</td><td>Newport Beach, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry San Diego</td><td>San Diego, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Post Ranch Inn</td><td>Big Sur, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rancho Bernardo Inn</td><td>San Diego, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rancho Valencia Resort &amp; Spa</td><td>Rancho Santa Fe, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Regent Santa Monica Beach</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rosewood Miramar Beach</td><td>Montecito, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rosewood Sand Hill</td><td>Menlo Park, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SIXTY Beverly Hills</td><td>Beverly Hills, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SLS Hotel, a Luxury Collection Hotel, Beverly Hills</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>San Francisco Proper Hotel</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sandbourne Santa Monica, Autograph Collection</td><td>Santa Monica, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Santa Monica Proper Hotel</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shade Hotel Manhattan Beach</td><td>Manhattan Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shade Hotel Redondo Beach</td><td>Redondo Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shashi Hotel Mountain View</td><td>Mountain View, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shore House at The Del, LXR Hotels &amp; Resorts</td><td>Coronado, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shutters on the Beach</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Signia by Hilton San Jose</td><td>San Jose, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel Los Angeles at Beverly Hills</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Solage, Auberge Collection</td><td>Calistoga, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Stanly Ranch, Auberge Collection</td><td>Napa, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sunset Tower Hotel</td><td>West Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Surf &amp; Sand Resort Laguna Beach</td><td>Laguna Beach, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>THE US GRANT, a Luxury Collection Hotel, San Diego</td><td>San Diego, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Taj Campton Place</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Terranea Resort &amp; Spa</td><td>Rancho Palos Verdes, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Beverly Hills Hotel &amp; Bungalows</td><td>Beverly Hills, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Clift Royal Sonesta San Francisco</td><td>San Francisco, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Estate Yountville</td><td>Yountville, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Exchange Sacramento, Curio Collection by Hilton</td><td>Sacramento, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Georgian</td><td>Santa Monica, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hollywood Grande, Autograph Collection</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hoxton, Downtown LA</td><td>Los Angeles, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Huntington Hotel</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn at Mattei&#x27;s Tavern, Auberge Collection</td><td>Los Olivos, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn at Rancho Santa Fe</td><td>Rancho Santa Fe, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Jay, Autograph Collection</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham Huntington, Pasadena</td><td>Pasadena, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Sonoma Resort, Autograph Collection</td><td>Sonoma, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Torrey Pines</td><td>La Jolla, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The London West Hollywood at Beverly Hills</td><td>West Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Madrona</td><td>Healdsburg, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Maybourne Beverly Hills</td><td>Beverly Hills, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Meritage Resort &amp; Spa</td><td>Napa, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Peninsula Beverly Hills</td><td>Beverly Hills, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Pierside Hotel Santa Monica</td><td>Santa Monica, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Portofino Hotel and Marina</td><td>Redondo Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Quail</td><td>Carmel, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch at Laguna Beach</td><td>Laguna Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Resort at Pelican Hill</td><td>Newport Coast, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Bacara, Santa Barbara</td><td>Santa Barbara, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Half Moon Bay</td><td>Half Moon Bay, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Laguna Niguel</td><td>Dana Point, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Lake Tahoe</td><td>Truckee, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Los Angeles</td><td>Los Angeles, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Marina del Rey in Los Angeles</td><td>Marina del Rey, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Rancho Mirage</td><td>Rancho Mirage, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, San Francisco</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sanctuary Beach Resort</td><td>Marina, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Seabird Ocean Resort and Spa</td><td>Oceanside, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis San Francisco</td><td>San Francisco, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sun Rose</td><td>West Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Valorian Los Angeles, Curio Collection by Hilton</td><td>West Hollywood, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Waterfront Beach Resort, a Hilton Hotel</td><td>Huntington Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The West Hollywood EDITION</td><td>West Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Anaheim Resort</td><td>Anaheim, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Palm Springs</td><td>Palm Springs, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Timber Cove Resort</td><td>Jenner, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Tommy Bahama Miramonte Resort &amp; Spa</td><td>Indian Wells, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Treehouse Silicon Valley</td><td>Sunnyvale, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>VEA Newport Beach, a Marriott Resort &amp; Spa</td><td>Newport Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Vespera Resort on Pismo Beach</td><td>Pismo Beach, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Santa Monica</td><td>Santa Monica, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Vinarosa Resort &amp; Spa</td><td>Santa Rosa, California</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Hollywood</td><td>Hollywood, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Beverly Hills</td><td>Beverly Hills, California</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Monarch Beach</td><td>Dana Point, California</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Colorado

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Aspen Meadows Resort</td><td>Aspen, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dunton Hot Springs</td><td>Dolores, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Denver</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort and Residences Vail</td><td>Vail, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Garden of the Gods Resort and Club</td><td>Colorado Springs, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Gateway Canyons Resort &amp; Spa</td><td>Gateway, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Vail</td><td>Vail, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Halcyon, a hotel in Cherry Creek</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Alpenrock Breckenridge, Curio Collection by Hilton</td><td>Breckenridge, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Clio, a Luxury Collection Hotel, Denver Cherry Creek</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Jerome, Auberge Collection</td><td>Aspen, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Polaris</td><td>Colorado Springs, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Claret Hotel</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Monaco Denver</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Boulder</td><td>Boulder, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Hotel Denver</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Snowmass</td><td>Snowmass Village, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>MOLLIE Aspen</td><td>Aspen, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Madeline Hotel &amp; Residences, Auberge Collection</td><td>Telluride, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Manor Vail Lodge</td><td>Vail, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Interlocken</td><td>Broomfield, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Beaver Creek Resort and Spa</td><td>Beaver Creek, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Populus Denver</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sonnenalp Hotel</td><td>Vail, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The ART Hotel Denver, Curio Collection by Hilton</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Arrabelle at Vail Square</td><td>Vail, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Brown Palace Hotel and Spa</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Crawford Hotel</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Eddy Taproom &amp; Hotel</td><td>Golden, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hythe, a Luxury Collection Resort, Vail</td><td>Vail, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Jacquard Hotel &amp; Rooftop, Autograph Collection</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Limelight Hotel Aspen</td><td>Aspen, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Little Nell</td><td>Aspen, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Maven Hotel at Dairy Block</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Mining Exchange</td><td>Colorado Springs, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Rally Hotel at McGregor Square</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ramble Hotel</td><td>Denver, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Bachelor Gulch</td><td>Avon, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Denver</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sebastian - Vail</td><td>Vail, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Aspen Resort</td><td>Aspen, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Riverfront Resort &amp; Spa, Avon, Vail Valley</td><td>Avon, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Denver</td><td>Denver, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Snowmass</td><td>Snowmass Village, Colorado</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viewline Resort Snowmass, Autograph Collection</td><td>Snowmass Village, Colorado</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Aspen</td><td>Aspen, Colorado</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Connecticut

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Belden House &amp; Mews</td><td>Litchfield, Connecticut</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Delamar West Hartford</td><td>West Hartford, Connecticut</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Madison Beach Hotel, Curio Collection by Hilton</td><td>Madison, Connecticut</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mayflower Inn and Spa, Auberge Collection</td><td>Washington, Connecticut</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### District of Columbia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad Washington, DC</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Washington DC</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Washington, D.C.</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel AKA Washington Circle</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Washington D.C. - The Wharf</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lyle Washington DC</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Washington D.C.</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Washington DC, The Wharf</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Riggs Washington DC</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rosewood Washington, D.C</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Royal Sonesta Washington DC Capitol Hill</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SIXTY DC</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Salamander Washington DC</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel Washington DC Lafayette Square</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Dupont Circle Hotel</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hay-Adams, Washington, D.C.</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Jefferson, Washington, DC</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Morrow Washington DC, Curio by Hilton</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Washington DC</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Washington D.C.</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin DC Downtown</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Washington DC</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Washington D.C.</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Washington DC</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Willard InterContinental Washington, D.C.</td><td>Washington, District of Columbia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Yours Truly DC, Vignette Collection by IHG</td><td>Washington, District of Columbia</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Florida

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel South Beach</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Acqualina Resort &amp; Residences on the Beach</td><td>Sunny Isles Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amara Cay Resort</td><td>Islamorada, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amrit Ocean Resort &amp; Residences</td><td>Riviera Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Miami Beach Resort and Spa</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Baker&#x27;s Cay Resort Key Largo, Curio Collection by Hilton</td><td>Key Largo, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Beach Club at The Boca Raton</td><td>Boca Raton, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Camp Creek Inn</td><td>Inlet Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton West Palm Beach - Downtown</td><td>West Palm Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carillon Miami Wellness Resort</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cloister at The Boca Raton</td><td>Boca Raton, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad Fort Lauderdale Beach</td><td>Fort Lauderdale, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad Orlando</td><td>Orlando, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>EAST Miami</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Eau Resort &amp; Spa Palm Beach</td><td>Manalapan, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Eden Roc Miami Beach</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Edgewater Beach Hotel</td><td>Naples, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Faena Miami Beach</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fontainebleau Miami Beach</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fort Lauderdale Marriott Harbor Beach Resort &amp; Spa</td><td>Fort Lauderdale, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Miami</td><td>Miami, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel and Residences Fort Lauderdale</td><td>Fort Lauderdale, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel at The Surf Club</td><td>Surfside, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Orlando at Walt Disney World Resort</td><td>Lake Buena Vista, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Palm Beach</td><td>Palm Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Tampa Bay</td><td>Tampa, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hammock Beach Golf Resort &amp; Spa</td><td>Palm Coast, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hawks Cay Resort</td><td>Duck Key, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel AKA West Palm</td><td>West Palm Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Effie Sandestin</td><td>Miramar Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Maren Fort Lauderdale Beach, Curio Collection by Hilton</td><td>Fort Lauderdale, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Clearwater Beach Resort &amp; Suites</td><td>Clearwater Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Coconut Point</td><td>Bonita Springs, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Coral Gables</td><td>Coral Gables, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn on Fifth</td><td>Naples, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Miami</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Isla Bella Beach Resort &amp; Spa</td><td>Marathon, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Clearwater Beach Resort &amp; Spa</td><td>Clearwater Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Marco Island</td><td>Marco Island, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Miami Turnberry Resort &amp; Spa</td><td>Aventura, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Orlando Bonnet Creek Resort and Spa</td><td>Orlando, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Orlando, Grande Lakes</td><td>Orlando, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Tampa Water Street</td><td>Tampa, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Jupiter Beach Resort &amp; Spa</td><td>Jupiter, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton EPIC Miami</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Surfcomber</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Vero Beach Hotel and Spa</td><td>Vero Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lido Beach Resort</td><td>Sarasota, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Little Palm Island Resort</td><td>Little Torch Key, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Coral Gables Hotel</td><td>Coral Gables, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Miami Beach Hotel</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Portofino Bay Hotel at Universal Orlando</td><td>Orlando, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Sapphire Falls at Universal Orlando</td><td>Orlando, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Luminary Hotel &amp; Co., Autograph Collection</td><td>Fort Myers, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Margaritaville Beach House Key West</td><td>Key West, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Margaritaville Hollywood Beach Resort</td><td>Hollywood, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Margaritaville Resort Orlando</td><td>Kissimmee, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mayfair House Hotel &amp; Garden</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moxy St. Petersburg Downtown</td><td>St. Petersburg, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mr. C Miami Coconut Grove</td><td>Miami, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Naples Beach Club, a Four Seasons Resort</td><td>Naples, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Naples Grande Beach Resort</td><td>Naples, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Miami Beach</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ocean Key Resort and Spa</td><td>Key West, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Oceans Edge Resort &amp; Marina</td><td>Key West, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Amelia Island Resort</td><td>Amelia Island, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Fort Lauderdale</td><td>Fort Lauderdale, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Orlando Resort at Championsgate</td><td>Championsgate, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Opal Grand Oceanfront Resort &amp; Spa</td><td>Delray Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Opal Sands Resort</td><td>Clearwater Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Orlando World Center Marriott</td><td>Orlando, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>PGA National Resort</td><td>Palm Beach Gardens, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pelican Grand Beach Resort</td><td>Fort Lauderdale, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pier Sixty-Six</td><td>Fort Lauderdale, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Reefhouse Resort &amp; Marina</td><td>Key Largo, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>SLS LUX Brickell</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Signia by Hilton Diplomat Beach Resort</td><td>Hollywood, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sunseeker Resort Florida Gulf Coast, Curio by Hilton</td><td>Charlotte Harbor, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Betsy South Beach</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Biltmore Hotel Miami - Coral Gables</td><td>Coral Gables, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Brazilian Court Hotel</td><td>Palm Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Breakers Palm Beach</td><td>Palm Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Brickell Arch, Luxury Collection by Marriott</td><td>Miami, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Don CeSar</td><td>St. Pete Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Henderson Beach Resort</td><td>Destin, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hiatus Clearwater Beach, Curio Collection by Hilton</td><td>Clearwater Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Miami Beach EDITION</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Palms Hotel &amp; Spa</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Perry Hotel &amp; Marina</td><td>Key West, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ray Hotel Delray Beach, Curio Collection by Hilton</td><td>Delray Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Reach Key West, Curio Collection by Hilton</td><td>Key West, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Coconut Grove, Miami</td><td>Miami, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Key Biscayne, Miami</td><td>Key Biscayne, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Naples, Tiburon</td><td>Naples, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Orlando, Grande Lakes</td><td>Orlando, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Residences Orlando, Grande Lakes</td><td>Orlando, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Amelia Island</td><td>Amelia Island, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Bal Harbour, Miami</td><td>Bal Harbour, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Fort Lauderdale</td><td>Fort Lauderdale, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Naples</td><td>Naples, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Sarasota</td><td>Sarasota, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, South Beach</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Seagate Hotel, Golf and Beach Club</td><td>Delray Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Setai, Miami Beach</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Shelborne By Proper</td><td>Miami, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Singer Oceanfront Resort Singer Island, Curio by Hilton</td><td>Riviera Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Bal Harbour Resort</td><td>Bal Harbour, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Longboat Key Resort</td><td>Longboat Key, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Standard Spa, Miami Beach</td><td>Miami Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Tampa EDITION</td><td>Tampa, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Vineta Hotel, Oetker Hotels</td><td>Palm Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Vinoy Resort and Golf Club, Autograph Collection</td><td>St. Petersburg, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thesis Hotel Miami Coral Gables, Curio Collection by Hilton</td><td>Coral Gables, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Three Waters Resort and Marina, a Tribute Portfolio Resort</td><td>Islamorada, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Tower at The Boca Raton</td><td>Boca Raton, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Treasure Island Beach Resort</td><td>Treasure Island, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Trump National Doral</td><td>Doral, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Fort Lauderdale</td><td>Fort Lauderdale, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W South Beach</td><td>Miami Beach, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Orlando</td><td>Orlando, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Walt Disney World Dolphin</td><td>Lake Buena Vista, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Walt Disney World Swan Reserve</td><td>Lake Buena Vista, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Walt Disney World Swan</td><td>Lake Buena Vista, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waterstone Resort &amp; Marina Boca Raton, Curio Collection by Hilton</td><td>Boca Raton, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>White Elephant Palm Beach</td><td>Palm Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wyndham Grand Clearwater Beach</td><td>Clearwater Beach, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wyndham Grand Jupiter at Harbourside Place</td><td>Jupiter, Florida</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Yacht Club at The Boca Raton</td><td>Boca Raton, Florida</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ette hotel</td><td>Kissimmee, Florida</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Georgia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Savannah</td><td>Savannah, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Candler Hotel, Curio Collection by Hilton</td><td>Atlanta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Atlanta Midtown</td><td>Atlanta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cloudland at McLemore Resort Lookout Mountain, Curio by Hilton</td><td>Rising Fawn, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>FORTH Atlanta</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Atlanta</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Atlanta</td><td>Atlanta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bardo Savannah</td><td>Savannah, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Phoenix Atlanta</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Buckhead Atlanta</td><td>Atlanta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Buckhead Atlanta</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Savannah Plant Riverside District</td><td>Savannah, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Jekyll Island Club</td><td>Jekyll Island, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Jekyll Ocean Club</td><td>Jekyll Island, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Atlanta Hotel</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Municipal Grand</td><td>Savannah, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Hotel at The Battery Atlanta</td><td>Atlanta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Perry Lane Hotel</td><td>Savannah, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sea Island Resort</td><td>Sea Island, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Alida Hotel, A Tribute Portfolio</td><td>Savannah, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Drayton Hotel Savannah, Curio Collection by Hilton</td><td>Savannah, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hamilton Alpharetta, Curio Collection by Hilton</td><td>Alpharetta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Reynolds, Lake Oconee</td><td>Greensboro, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Atlanta</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Atlanta</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Tess, Autograph Collection</td><td>Atlanta, Georgia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Whitley, A Luxury Collection Hotel, Atlanta Buckhead</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Savannah</td><td>Savannah, Georgia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Atlanta Buckhead</td><td>Atlanta, Georgia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hawaii

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>&#x27;Alohilani Resort Waikiki Beach</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Hanalei Bay</td><td>Princeville, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz Maui at Wailea Resort</td><td>Wailea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Espacio The Jewel of Waikiki</td><td>Honolulu, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Kea Lani, Maui</td><td>Wailea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Orchid, Hawaii</td><td>Kohala Coast, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Hualalai</td><td>Kailua-Kona, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Lana&#x27;i</td><td>Lanai City, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Maui at Wailea</td><td>Wailea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Oahu at Ko Olina</td><td>Kapolei, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Kaua`i Resort &amp; Spa</td><td>Koloa, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Wailea, A Waldorf Astoria Resort</td><td>Wailea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Halekulani</td><td>Honolulu, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Halepuna Waikiki by Halekulani</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hilton Waikoloa Village</td><td>Waikoloa, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hoolei Villas at Grand Wailea</td><td>Wailea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Wailea, Relais &amp; Chateaux</td><td>Wailea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Maui Resort &amp; Spa</td><td>Lahaina, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ka La&#x27;i Waikiki Beach, LXR Hotels &amp; Resorts</td><td>Honolulu, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ko&#x27;a Kea Resort on Poipu Beach</td><td>Koloa, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kona Village, A Rosewood Resort</td><td>Kailua-Kona, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mauna Kea Beach Hotel, Autograph Collection</td><td>Waimea, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mauna Lani, Auberge Collection</td><td>Kohala Coast, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moana Surfrider, A Westin Resort &amp; Spa</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>OUTRIGGER Reef Waikiki Beach Resort</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Prince Waikiki</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Romer House Waikiki</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sensei Lana&#x27;i, A Four Seasons Resort</td><td>Lanai City, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sheraton Waikiki Beach Resort</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Kahala Hotel &amp; Resort</td><td>Honolulu, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Resort at Kapalua Bay, Maui</td><td>Lahaina, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Maui, Kapalua</td><td>Kapalua, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton O&#x27;ahu, Turtle Bay</td><td>Kahuku, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Residences, Waikiki Beach</td><td>Honolulu, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Royal Hawaiian, a Luxury Collection Resort, Waikiki</td><td>Honolulu, Hawaii</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Royal Sonesta Kauai Resort</td><td>Lihue, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Maui Resort &amp; Spa</td><td>Lahaina, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wailea Beach Resort - Marriott, Maui</td><td>Wailea, Hawaii</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wayfinder Waikiki</td><td>Honolulu, Hawaii</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Idaho

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Limelight Hotel Ketchum</td><td>Ketchum, Idaho</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sun Valley Resort</td><td>Sun Valley, Idaho</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Illinois

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Chicago Central Loop</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Chicago Millennium Park</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel 55 Chicago Downtown</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Chicago Magnificent Mile</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Gray Hotel</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>L7 Chicago by Lotte</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Chicago Downtown</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nobu Hotel Chicago</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sable at Navy Pier Chicago, Curio Collection by Hilton</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel Chicago Magnificent Mile</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Gwen, a Luxury Collection Hotel</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hoxton Chicago</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham, Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Peninsula Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Royal Sonesta Chicago Downtown</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Talbott, Autograph Collection</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Trump International Hotel &amp; Tower Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Viceroy Chicago</td><td>Chicago, Illinois</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Chicago</td><td>Chicago, Illinois</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Iowa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Surety Hotel Des Moines, Autograph Collection</td><td>Des Moines, Iowa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Kentucky

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>21c Museum Hotel Louisville</td><td>Louisville, Kentucky</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bourre Bonne Louisville, Curio Collection by Hilton</td><td>Louisville, Kentucky</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Distil, An Autograph Collection</td><td>Louisville, Kentucky</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Louisville Hotel</td><td>Louisville, Kentucky</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Louisiana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton New Orleans - Downtown</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel New Orleans</td><td>New Orleans, Louisiana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Peter and Paul</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Saint Vincent</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel de la Poste - French Quarter, a Renaissance Hotel</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric French Quarter</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott New Orleans</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Fontenot</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Le Meridien New Orleans</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews New Orleans</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Maison Metier by Hyatt</td><td>New Orleans, Louisiana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>New Orleans Marriott Warehouse Arts District Hotel</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Barnett by Hyatt</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Eliza Jane, Autograph Collection</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, New Orleans</td><td>New Orleans, Louisiana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Roosevelt New Orleans, a Waldorf Astoria Hotel</td><td>New Orleans, Louisiana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Windsor Court, New Orleans</td><td>New Orleans, Louisiana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels New Orleans</td><td>New Orleans, Louisiana</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Maine

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Camden Harbour Inn</td><td>Camden, Maine</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Portland Waterfront</td><td>Portland, Maine</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn by the Sea</td><td>Cape Elizabeth, Maine</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Press Hotel, Autograph Collection</td><td>Portland, Maine</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>White Barn Inn, Auberge Collection</td><td>Kennebunk, Maine</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Maryland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Annapolis Waterfront Hotel, Autograph Collection</td><td>Annapolis, Maryland</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Baltimore Harbor Point</td><td>Baltimore, Maryland</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Baltimore</td><td>Baltimore, Maryland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Inn at Perry Cabin</td><td>St. Michaels, Maryland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Baltimore</td><td>Baltimore, Maryland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Revival Baltimore</td><td>Baltimore, Maryland</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ivy Hotel Baltimore</td><td>Baltimore, Maryland</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Massachusetts

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Boston Harbor Hotel</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Chatham Bars Inn Resort &amp; Spa</td><td>Chatham, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Chatham Inn Relais &amp; Chateaux</td><td>Chatham, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Encore Boston Harbor</td><td>Everett, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Copley Plaza</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel One Dalton Street, Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Harbor View Hotel</td><td>Edgartown, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel AKA Back Bay</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Boston</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Marlowe Hotel</td><td>Cambridge, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mandarin Oriental, Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Miraval Berkshires</td><td>Lenox, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Boston Hotel at the Seaport</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Raffles Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Red Jacket Beach Resort &amp; Spa</td><td>South Yarmouth, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Atlas Hotel</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Charles Hotel</td><td>Cambridge, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Envoy Hotel, Autograph Collection</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn at Hastings Park</td><td>Lexington, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham, Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Nantucket Hotel and Resort</td><td>Nantucket, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Newbury Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Boston</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Wauwinet</td><td>Nantucket, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Westin Copley Place, Boston</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Whitney Hotel Boston</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Winnetu Oceanside Resort</td><td>Edgartown, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Boston</td><td>Boston, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wequassett Resort and Golf Club</td><td>Harwich, Massachusetts</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>White Elephant</td><td>Nantucket, Massachusetts</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>XV Beacon Hotel</td><td>Boston, Massachusetts</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Michigan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Grand Rapids Downtown</td><td>Grand Rapids, Michigan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Daxton Hotel Birmingham, Curio Collection by Hilton</td><td>Birmingham, Michigan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Detroit Foundation Hotel</td><td>Detroit, Michigan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Shinola Hotel</td><td>Detroit, Michigan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Godfrey Detroit, Curio Collection by Hilton</td><td>Detroit, Michigan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn at Bay Harbor</td><td>Bay Harbor, Michigan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Townsend Hotel</td><td>Birmingham, Michigan</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Minnesota

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Minneapolis - Mill District</td><td>Minneapolis, Minnesota</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Emery, an Autograph Collection Hotel</td><td>Minneapolis, Minnesota</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Minneapolis</td><td>Minneapolis, Minnesota</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Ivy, a Luxury Collection Hotel, Minneapolis</td><td>Minneapolis, Minnesota</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Downtown Minneapolis</td><td>Minneapolis, Minnesota</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hotel Landing</td><td>Wayzata, Minnesota</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Marquette Hotel, Curio Collection by Hilton</td><td>Minneapolis, Minnesota</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Missouri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>21c Museum Hotel St. Louis</td><td>St. Louis, Missouri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Crossroads Hotel</td><td>Kansas City, Missouri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel St. Louis</td><td>St. Louis, Missouri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Live by Loews - St Louis</td><td>St. Louis, Missouri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Kansas City Hotel</td><td>Kansas City, Missouri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, St. Louis</td><td>St. Louis, Missouri</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Big Sky</td><td>Big Sky, Montana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>One&amp;Only Moonlight Basin</td><td>Big Sky, Montana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Paws Up Montana</td><td>Greenough, Montana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch at Rock Creek</td><td>Philipsburg, Montana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nevada

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ARIA Resort &amp; Casino</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ARIA Sky Suites</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bellagio</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad Las Vegas at Resorts World</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Crockfords Las Vegas, LXR Hotels &amp; Resorts</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Durango Casino &amp; Resort</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Edgewood Tahoe</td><td>Stateline, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fontainebleau Las Vegas</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Las Vegas</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Lake Tahoe Resort, Spa and Casino</td><td>Incline Village, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Las Vegas Resort &amp; Spa</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Palazzo at The Venetian</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park MGM Las Vegas</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Red Rock Casino Resort &amp; Spa</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Cosmopolitan of Las Vegas</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Reserve at Park MGM</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Venetian Resort Las Vegas</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels Las Vegas, Curio Collection by Hilton</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Las Vegas</td><td>Las Vegas, Nevada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Las Vegas</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wynn and Encore Las Vegas</td><td>Las Vegas, Nevada</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### New Jersey

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Asbury Ocean Club</td><td>Asbury Park, New Jersey</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Congress Hall Hotel</td><td>Cape May, New Jersey</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Graduate by Hilton Princeton</td><td>Princeton, New Jersey</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Natirar</td><td>Peapack, New Jersey</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Asbury Hotel</td><td>Asbury Park, New Jersey</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Hoboken</td><td>Hoboken, New Jersey</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### New Mexico

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bishop&#x27;s Lodge, Auberge Collection</td><td>Santa Fe, New Mexico</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort Rancho Encantado Santa Fe</td><td>Santa Fe, New Mexico</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rosewood Inn of the Anasazi, Santa Fe</td><td>Santa Fe, New Mexico</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn of The Five Graces</td><td>Santa Fe, New Mexico</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### New York

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Brooklyn Bridge</td><td>Brooklyn, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Central Park</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>11 Howard</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Ace Hotel Brooklyn</td><td>Brooklyn, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Aman New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Andaz 5th Avenue</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Baccarat Hotel New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canoe Place Inn &amp; Cottages</td><td>Hampton Bays, New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Casa Cipriani New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad New York Downtown</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dream Downtown</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Equinox Hotel New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Faena New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel New York Downtown</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Gansevoort Meatpacking</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Gild Hall, A Thompson Hotel</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hard Rock Hotel New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Barriere Fouquet&#x27;s New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Saranac, Curio Collection by Hilton</td><td>Saranac Lake, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Times Square New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Times Square, New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Essex House New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Eventi</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Theta New York - Times Square</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Regency New York Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lotte New York Palace</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mandarin Oriental, New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ModernHaus SoHo</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montauk Yacht Club</td><td>Montauk, New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moxy Brooklyn Williamsburg</td><td>Brooklyn, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moxy NYC East Village</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Moxy NYC Lower East Side</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nine Orchard</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>PUBLIC Hotels</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Hyatt New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Park Lane New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Manhattan West</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Refinery Hotel</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Scribner&#x27;s Catskill Lodge</td><td>Hunter, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Smyth Tribeca</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Soho Grand Hotel</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sonesta White Plains Downtown</td><td>White Plains, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Adelphi Hotel</td><td>Saratoga Springs, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Beekman, A Thompson Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Carlyle, A Rosewood Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Chatwal, New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Fifth Avenue Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Garden City Hotel</td><td>Garden City, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Greenwich Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hoxton, Williamsburg</td><td>Brooklyn, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Knickerbocker Hotel</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lake House on Canandaigua</td><td>Canandaigua, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Langham, New York, Fifth Avenue</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lowell, New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Manner</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Mark</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Mercer Hotel</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ned NoMad</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The New York EDITION</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Peninsula New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Pierre, New York, a Taj Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Plaza</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Pridwin Hotel</td><td>Shelter Island, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ranch Hudson Valley</td><td>Sloatsburg, New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton New York, Central Park</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton New York, NoMad</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Rockaway Hotel + Spa</td><td>Queens, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Roxy Hotel New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Standard, East Village</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Standard, High Line</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Surrey, A Corinthia Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Times Square EDITION</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Towers at Lotte New York Palace</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Twenty Two New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Wall Street Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Whitby Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The William Vale</td><td>Brooklyn, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Central Park New York</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Troutbeck</td><td>Amenia, New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Trump International Hotel &amp; Tower New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels New York City</td><td>New York</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W New York - Union Square</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria New York</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Warren Street Hotel</td><td>New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wildflower Farms, Auberge Collection</td><td>Gardiner, New York</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wylder Hotel Windham</td><td>Windham, New York</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### North Carolina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Cataloochee Ranch</td><td>Maggie Valley, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Hotel Charlotte, Autograph Collection</td><td>Charlotte, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Lodge Asheville, Autograph Collection</td><td>Asheville, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Tryon Park Hotel</td><td>Charlotte, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Charlotte Hotel</td><td>Charlotte, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ballantyne, a Luxury Collection Hotel, Charlotte</td><td>Charlotte, North Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Fearrington House</td><td>Pittsboro, North Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Foundry Hotel Asheville, Curio Collection by Hilton</td><td>Asheville, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ivey&#x27;s Hotel</td><td>Charlotte, North Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Omni Grove Park Inn Resort and Spa</td><td>Asheville, North Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Charlotte</td><td>Charlotte, North Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sanderling</td><td>Duck, North Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Umstead Hotel &amp; Spa</td><td>Cary, North Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Trailborn Surf and Sound Resort</td><td>Wrightsville Beach, North Carolina</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ohio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>21c Museum Hotel Cincinnati</td><td>Cincinnati, Ohio</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Schofield Hotel</td><td>Cleveland, Ohio</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Le Meridien Columbus, The Joseph</td><td>Columbus, Ohio</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Junto</td><td>Columbus, Ohio</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Cleveland</td><td>Cleveland, Ohio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Oklahoma

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Oklahoma City Hotel</td><td>Oklahoma City, Oklahoma</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Skirvin Oklahoma City, a Hilton Hotel</td><td>Oklahoma City, Oklahoma</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Tulsa Club Hotel, Curio Collection by Hilton</td><td>Tulsa, Oklahoma</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Oregon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>CASCADA Thermal Springs + Hotel</td><td>Portland, Oregon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Portland - Pearl District</td><td>Portland, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Headlands Coastal Lodge and Spa</td><td>Pacific City, Oregon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hilton Portland Downtown</td><td>Portland, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Vintage Portland</td><td>Portland, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton RiverPlace Hotel</td><td>Portland, Oregon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Riverhouse Lodge</td><td>Bend, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Royal Sonesta Portland</td><td>Portland, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sentinel</td><td>Portland, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sunriver Resort</td><td>Sunriver, Oregon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Duniway Portland</td><td>Portland, Oregon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Portland</td><td>Portland, Oregon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>the Nines, a Luxury Collection Hotel, Portland</td><td>Portland, Oregon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pennsylvania

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>AKA Rittenhouse Square</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Philadelphia Center City</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Pittsburgh</td><td>Pittsburgh, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Philadelphia at Comcast Center</td><td>Philadelphia, Pennsylvania</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Anna &amp; Bel</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Rittenhouse Square Philadelphia</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Monaco Philadelphia</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Monaco Pittsburgh</td><td>Pittsburgh, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Loews Philadelphia Hotel</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Nemacolin</td><td>Farmington, Pennsylvania</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Bedford Springs Resort and Spa</td><td>Bedford, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sofitel Philadelphia at Rittenhouse Square</td><td>Philadelphia, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Bellevue Hotel</td><td>Philadelphia, Pennsylvania</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Industrialist Hotel, Pittsburgh</td><td>Pittsburgh, Pennsylvania</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Rittenhouse</td><td>Philadelphia, Pennsylvania</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Rhode Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Brenton Hotel</td><td>Newport, Rhode Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Chanler at Cliff Walk</td><td>Newport, Rhode Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Vanderbilt, Auberge Collection</td><td>Newport, Rhode Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### South Carolina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Emeline</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Hotel Charleston, Autograph Collection</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Bohemian Lodge Greenville, Autograph Collection</td><td>Greenville, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Bennett</td><td>Charleston, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mills House Charleston, Curio Collection by Hilton</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Palmetto Bluff</td><td>Bluffton, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Hilton Head Oceanfront Resort</td><td>Hilton Head Island, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sonesta Resort Hilton Head Island</td><td>Hilton Head Island, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Beach Club at Charleston Harbor Resort &amp; Marina</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Charleston Place</td><td>Charleston, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Dewberry</td><td>Charleston, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Dunlin, Auberge Collection</td><td>Johns Island, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Inn &amp; Club at Harbour Town</td><td>Hilton Head Island, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Loutrel</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Palmetto Hotel</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Pinch Charleston</td><td>Charleston, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ryder</td><td>Charleston, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Sanctuary at Kiawah Island Golf Resort</td><td>Kiawah Island, South Carolina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Wild Dunes Resort</td><td>Isle of Palms, South Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Zero George Street</td><td>Charleston, South Carolina</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tennessee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Nashville</td><td>Nashville, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Memphis Downtown Beale Street</td><td>Memphis, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Nashville Downtown the Gulch</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Conrad Nashville</td><td>Nashville, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Dream Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Nashville</td><td>Nashville, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Fraye Nashville, Curio Collection by Hilton</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Downtown Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Aertson Hotel</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Margaritaville Hotel Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Noelle</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Nashville Hotel</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Southall Farm &amp; Inn</td><td>Franklin, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Central Station Memphis, Curio Collection by Hilton</td><td>Memphis, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Harpeth Franklin Downtown, Curio Collection by Hilton</td><td>Franklin, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Hermitage Hotel</td><td>Nashville, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Joseph, a Luxury Collection Hotel, Nashville</td><td>Nashville, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Read House Hotel</td><td>Chattanooga, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Tennessean Hotel</td><td>Knoxville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Union Station Nashville Yards</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Nashville</td><td>Nashville, Tennessee</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Nashville</td><td>Nashville, Tennessee</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Texas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Austin Proper Hotel</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Bowie House, Auberge Collection</td><td>Fort Worth, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>C. Baldwin, Curio Collection by Hilton</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Austin Downtown</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton Dallas Uptown</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Canopy by Hilton San Antonio Riverwalk</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Carpenter Hotel</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Commodore Perry Estate, Auberge Collection</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Austin</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Austin</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Houston</td><td>Houston, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Crescent Court</td><td>Dallas, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Emma at Pearl, San Antonio</td><td>San Antonio, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Granduca Houston</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Magdalena</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Saint Augustine</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Saint Cecilia</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Swexan</td><td>Dallas, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Van Zandt</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel ZaZa Austin</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel ZaZa Dallas</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel ZaZa Memorial City</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel ZaZa Museum District</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Houston Grand Hotel–River Oaks</td><td>Houston, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Congress Avenue Austin</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Hill Country Resort</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Regency Lost Pines Resort and Spa</td><td>Lost Pines, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Houston</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental San Antonio Riverwalk</td><td>San Antonio, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Dallas Arts District</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Houston Downtown</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott Houston by the Galleria</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>JW Marriott San Antonio Hill Country Resort &amp; Spa</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Harper</td><td>Fort Worth, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Santo San Antonio-Riverwalk</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>LINE Austin</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Live By Loews - Arlington</td><td>Arlington, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Miraval Austin</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Mokara Hotel &amp; Spa</td><td>San Antonio, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Austin Hotel Downtown</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Barton Creek Resort</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Dallas Hotel, Downtown</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Fort Worth Hotel</td><td>Fort Worth, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Houston Hotel</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni La Mansion del Rio</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Las Colinas Hotel</td><td>Irving, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni PGA Frisco Resort</td><td>Frisco, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rosewood Mansion on Turtle Creek, Dallas</td><td>Dallas, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Signia by Hilton La Cantera Resort &amp; Spa</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Crescent Hotel, Fort Worth</td><td>Fort Worth, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Houstonian Hotel Club &amp; Spa</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Joule</td><td>Dallas, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Kimpton Pittman Hotel</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lancaster Hotel</td><td>Houston, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Loren Hotel Austin</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Monarch San Antonio, Curio Collection by Hilton</td><td>San Antonio, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Otis Hotel Austin, Autograph Collection</td><td>Austin, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Plaza Hotel Pioneer Park</td><td>El Paso, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Post Oak Hotel at Uptown Houston</td><td>Houston, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton Dallas, Las Colinas</td><td>Irving, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Dallas</td><td>Dallas, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Statler Dallas, Curio Collection by Hilton</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Austin</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Dallas</td><td>Dallas, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Houston</td><td>Houston, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson San Antonio Riverwalk</td><td>San Antonio, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Virgin Hotels Dallas</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Austin</td><td>Austin, Texas</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>W Dallas</td><td>Dallas, Texas</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Utah

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amangiri</td><td>Canyon Point, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Asher Adams, an Autograph Collection</td><td>Salt Lake City, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Black Desert Resort</td><td>Ivins, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Black Rock Mountain Resort</td><td>Heber City, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Goldener Hirsch, Auberge Collection</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Grand Hyatt Deer Valley</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hyatt Centric Park City</td><td>Park City, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Hotel Monaco Salt Lake City</td><td>Salt Lake City, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Montage Deer Valley</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Pendry Park City</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Snowpine Lodge</td><td>Alta, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Stein Eriksen Lodge Deer Valley</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sundance Mountain Resort</td><td>Sundance, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Chateaux Deer Valley</td><td>Park City, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Grand America Hotel</td><td>Salt Lake City, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Blue Sky, Auberge Collection</td><td>Wanship, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Residences at Grand Hyatt Deer Valley</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The St. Regis Deer Valley</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>ULUM Moab</td><td>La Sal, Utah</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Waldorf Astoria Park City</td><td>Park City, Utah</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vermont

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Spruce Peak</td><td>Stowe, Vermont</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Woodstock Inn &amp; Resort</td><td>Woodstock, Vermont</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Virginia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel AKA Alexandria</td><td>Alexandria, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Heron Alexandria Old Town, Curio Collection by Hilton</td><td>Alexandria, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Keswick Hall</td><td>Keswick, Virginia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton The Forum Hotel</td><td>Charlottesville, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Omni Charlottesville Hotel</td><td>Charlottesville, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Quirk Hotel Richmond</td><td>Richmond, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Salamander Middleburg</td><td>Middleburg, Virginia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Jefferson Hotel</td><td>Richmond, Virginia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at Primland, Auberge Collection</td><td>Meadows of Dan, Virginia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Omni Homestead Resort</td><td>Hot Springs, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Pentagon City</td><td>Arlington, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Ritz-Carlton, Tysons Corner</td><td>McLean, Virginia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Tides Inn</td><td>Irvington, Virginia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Virginian Lynchburg, Curio Collection by Hilton</td><td>Lynchburg, Virginia</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Washington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>1 Hotel Seattle</td><td>Seattle, Washington</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Casia Lodge and Ranch Adults Only</td><td>Twisp, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Fairmont Olympic Hotel</td><td>Seattle, Washington</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Hotel Seattle</td><td>Seattle, Washington</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel 1000</td><td>Seattle, Washington</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Theodore Seattle Downtown, Tapestry by Hilton</td><td>Seattle, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>InterContinental Seattle Bellevue</td><td>Bellevue, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Kimpton Palladian Hotel</td><td>Seattle, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Lotte Hotel Seattle</td><td>Seattle, Washington</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Populus Seattle</td><td>Seattle, Washington</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Salish Lodge &amp; Spa</td><td>Snoqualmie, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Alexis Royal Sonesta Hotel</td><td>Seattle, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Charter Hotel Seattle, Curio Collection by Hilton</td><td>Seattle, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Edgewater</td><td>Seattle, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Lodge at St. Edward State Park Seattle/Kirkland</td><td>Kenmore, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Woodmark Hotel &amp; Still Spa on Lake Washington</td><td>Kirkland, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Thompson Seattle</td><td>Seattle, Washington</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Willows Lodge</td><td>Woodinville, Washington</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Wisconsin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The American Club</td><td>Kohler, Wisconsin</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Wyoming

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Amangani</td><td>Jackson, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Brush Creek Ranch Collection</td><td>Saratoga, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Caldera House</td><td>Teton Village, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Four Seasons Resort and Residences Jackson Hole</td><td>Teton Village, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Hotel Terra Jackson Hole</td><td>Teton Village, Wyoming</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Rusty Parrot Lodge and Spa</td><td>Jackson, Wyoming</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Sylvan Lodge</td><td>Jackson, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>Teton Mountain Lodge and Spa</td><td>Teton Village, Wyoming</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="North America" data-country="United States"><td>The Cloudveil</td><td>Jackson, Wyoming</td><td>FHR</td><td>—</td></tr>
</tbody></table>

## Caribbean

### Anguilla

#### Wyoming

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Aurora Anguilla Resort &amp; Golf Club</td><td>Rendezvous Bay, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Cap Juluca, A Belmond Hotel, Anguilla</td><td>Maundays Bay, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Four Seasons Resort and Residences Anguilla</td><td>Barnes Bay, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Malliouhana Resort Anguilla</td><td>Meads Bay, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Anguilla"><td>Zemi Beach House - Anguilla</td><td>The Valley, Wyoming</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Antigua

#### Wyoming

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua"><td>Carlisle Bay</td><td>St. Mary&#x27;s, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua"><td>Hermitage Bay</td><td>St. John&#x27;s, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Antigua"><td>Jumby Bay Island, Oetker Hotels</td><td>Jumby Bay Island, Wyoming</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Aruba

#### Wyoming

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>Hyatt Regency Aruba Resort, Spa &amp; Casino</td><td>Palm Beach, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>The Ritz-Carlton, Aruba</td><td>Palm Beach, Wyoming</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>The St. Regis Aruba Resort</td><td>Palm Beach, Wyoming</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Palm Beach

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Aruba"><td>Aruba Marriott Resort &amp; Stellaris Casino</td><td>Palm Beach</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Bahamas

#### Great Exuma

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>Grand Isle Resort &amp; Residences</td><td>Great Exuma</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nassau

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>Goldwynn Resort &amp; Residences</td><td>Nassau</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>Grand Hyatt Baha Mar</td><td>Nassau</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>Margaritaville Beach Resort Nassau</td><td>Nassau</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>SLS Baha Mar</td><td>Nassau</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Paradise Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Coral at Atlantis</td><td>Paradise Island</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Reef at Atlantis</td><td>Paradise Island</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bahamas"><td>The Royal at Atlantis</td><td>Paradise Island</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Barbados

#### Paradise Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Barbados"><td>Sandy Lane</td><td>St. James, Paradise Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### St. James

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Barbados"><td>Fairmont Royal Pavilion</td><td>St. James</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Bermuda

#### St. James

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>Hamilton Princess &amp; Beach Club, A Fairmont Managed Hotel</td><td>Hamilton, St. James</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>Rosewood Bermuda</td><td>Tucker&#x27;s Town, St. James</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>The Loren at Pink Beach</td><td>Tucker&#x27;s Town, St. James</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>The St. Regis Bermuda Resort</td><td>St. George&#x27;s, St. James</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sandys

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Bermuda"><td>Cambridge Beaches Resort &amp; Spa</td><td>Sandys</td><td>THC</td><td>—</td></tr>
</tbody></table>

### British Virgin Islands

#### Sandys

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="British Virgin Islands"><td>Peter Island Resort</td><td>Peter Island, Sandys</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="British Virgin Islands"><td>Rosewood Little Dix Bay</td><td>Virgin Gorda, Sandys</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Cayman Islands

#### Sandys

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Kimpton Seafire Resort + Spa</td><td>Grand Cayman, Sandys</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Palm Heights</td><td>Grand Cayman, Sandys</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>The Ritz-Carlton, Grand Cayman</td><td>Grand Cayman, Sandys</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Grand Cayman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Grand Cayman Marriott Resort</td><td>Grand Cayman</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>Hotel Indigo Grand Cayman</td><td>Grand Cayman</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Cayman Islands"><td>The Westin Grand Cayman Seven Mile Beach Resort &amp; Spa</td><td>Grand Cayman</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Curaçao

#### Willemstad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Curaçao"><td>Curacao Marriott Beach Resort</td><td>Willemstad</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Curaçao"><td>Mangrove Beach Corendon Curacao All-Inclusive Resort, Curio by Hilton</td><td>Willemstad</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Curaçao"><td>The Rif at Mangrove Beach Corendon Curacao All-Inclusive, Curio by Hilton</td><td>Willemstad</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Dominica

#### Willemstad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominica"><td>Secret Bay</td><td>Portsmouth, Willemstad</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Portsmouth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominica"><td>InterContinental Dominica Cabrits Resort &amp; Spa</td><td>Portsmouth</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Dominican Republic

#### Portsmouth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Amanera</td><td>Playa Grande, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Casa de Campo Resort &amp; Villas</td><td>La Romana, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Eden Roc at Cap Cana</td><td>Punta Cana, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Paradisus Grand Cana All Suites</td><td>Bavaro, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>The Ocean Club, a Luxury Collection resort, Costa Norte</td><td>Sosua, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>The St. Regis Cap Cana Resort</td><td>Punta Cana, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Tortuga Bay Puntacana Resort &amp; Club</td><td>Punta Cana, Portsmouth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>W Punta Cana, Adult All-Inclusive</td><td>Higuey, Portsmouth</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Miches

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Zemi Miches Punta Cana All-Inclusive Resort, Curio Collection by Hilton</td><td>Miches</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Puerto Plata

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Casa Colonial Beach and Spa</td><td>Puerto Plata</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Punta Cana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Hyatt Zilara Cap Cana</td><td>Punta Cana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Hyatt Ziva Cap Cana</td><td>Punta Cana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Secrets Tides Punta Cana</td><td>Punta Cana</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Zel Punta Cana – All Suites</td><td>Punta Cana</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Santiago de los Caballeros

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Hotel Santiago, Curio Collection by Hilton</td><td>Santiago de los Caballeros</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Santo Domingo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Dominican Republic"><td>Kimpton Las Mercedes</td><td>Santo Domingo</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Grenada

#### Santo Domingo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada"><td>Calabash Hotel</td><td>St. George&#x27;s, Santo Domingo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada"><td>Silversands Grenada</td><td>St. George&#x27;s, Santo Domingo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Grenada"><td>Six Senses La Sagesse Grenada</td><td>St. David, Santo Domingo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Honduras

#### Santo Domingo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Honduras"><td>Kimpton Grand Roatan Resort and Spa</td><td>Roatan, Santo Domingo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Jamaica

#### Santo Domingo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>Half Moon</td><td>Montego Bay, Santo Domingo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>Round Hill Hotel and Villas</td><td>Montego Bay, Santo Domingo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montego Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>S Hotel Montego Bay</td><td>Montego Bay</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ocho Rios

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Jamaica"><td>Jamaica Inn</td><td>Ocho Rios</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Puerto Rico

#### Ocho Rios

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Condado Vanderbilt Hotel</td><td>San Juan, Ocho Rios</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Dorado Beach, a Ritz-Carlton Reserve</td><td>Dorado, Ocho Rios</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Four Seasons Resort and Residences Puerto Rico</td><td>Rio Grande, Ocho Rios</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Residences at Dorado Beach, a Ritz-Carlton Reserve</td><td>Dorado, Ocho Rios</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Carolina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Fairmont El San Juan Hotel</td><td>Carolina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>The Royal Sonesta San Juan</td><td>Carolina</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Rio Grande

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Hyatt Regency Grand Reserve Puerto Rico</td><td>Rio Grande</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### San Juan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Condado Ocean Club</td><td>San Juan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Puerto Rico"><td>Hotel El Convento</td><td>San Juan</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Saint Barthelemy

#### San Juan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Cheval Blanc St-Barth</td><td>Baie des Flamands, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Eden Rock - St Barths, Oetker Hotels</td><td>St. Jean Bay, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Fouquet&#x27;s Saint-Barth</td><td>Gustavia, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Gyp Sea Saint Barth</td><td>Saint Barthelemy, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Hotel Christopher</td><td>Pointe Milou, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Hotel Le Toiny</td><td>Toiny, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Le Barthelemy Hotel &amp; Spa</td><td>Grand Cul-de-Sac, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Le Sereno St. Barths</td><td>Grand Cul-de-Sac, San Juan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthelemy"><td>Rosewood Le Guanahani St. Barth</td><td>Grand Cul-de-Sac, San Juan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Saint Barthélemy

#### Gustavia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Barthélemy"><td>Hotel Manapany</td><td>Gustavia</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Saint Kitts and Nevis

#### Gustavia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Kitts and Nevis"><td>Four Seasons Resort Nevis</td><td>Charlestown, Gustavia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Kitts and Nevis"><td>Park Hyatt St. Kitts Christophe Harbour</td><td>Basseterre, Gustavia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Basseterre

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Kitts and Nevis"><td>Koi Resort Saint Kitts, Curio Collection by Hilton</td><td>Basseterre</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Gingerland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Kitts and Nevis"><td>Golden Rock Inn</td><td>Gingerland</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Saint Lucia

#### Gingerland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Lucia"><td>Cap Maison Resort &amp; Spa</td><td>Gros Islet, Gingerland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Lucia"><td>Jade Mountain</td><td>Soufriere, Gingerland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Lucia"><td>Ladera Resort Saint Lucia</td><td>Soufriere, Gingerland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Lucia"><td>Sugar Beach, A Viceroy Resort</td><td>Soufriere, Gingerland</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Castries

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Lucia"><td>Harbor Club St. Lucia, Curio Collection by Hilton</td><td>Castries</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Saint Martin

#### Castries

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Martin"><td>La Samanna, A Belmond Hotel, St Martin</td><td>Terres Basses, Castries</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Saint Vincent and The Grenadines

#### Castries

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Saint Vincent and The Grenadines"><td>Mandarin Oriental, Canouan</td><td>Canouan Island, Castries</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### The Bahamas

#### Castries

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="The Bahamas"><td>Pink Sands Resort</td><td>Dunmore Town, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="The Bahamas"><td>Rosewood Baha Mar</td><td>Nassau, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="The Bahamas"><td>The Cove Eleuthera</td><td>Gregory Town, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="The Bahamas"><td>The Cove at Atlantis</td><td>Paradise Island, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="The Bahamas"><td>The Ocean Club, A Four Seasons Resort, Bahamas</td><td>Paradise Island, Castries</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Turks and Caicos Islands

#### Castries

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Amanyara</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Ambergris Cay</td><td>Big Ambergris Cay, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Beach Enclave</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>COMO Parrot Cay</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Grace Bay Club</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Pine Cay</td><td>Pine Cay, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Salterra, a Luxury Collection Resort &amp; Spa, South Caicos</td><td>Cockburn Harbour, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>The Ritz-Carlton Residences, Turks &amp; Caicos</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>The Strand Turks and Caicos</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Wymara Resort + Villas</td><td>Providenciales, Castries</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Providenciales

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="Turks and Caicos Islands"><td>Hotel Indigo Turks and Caicos</td><td>Providenciales</td><td>THC</td><td>—</td></tr>
</tbody></table>

### U.S. Virgin Islands

#### Providenciales

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands"><td>Buoy Haus Beach Resort St. Thomas, Autograph Collection</td><td>St. Thomas, Providenciales</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands"><td>The Ritz-Carlton, St. Thomas</td><td>St. Thomas, Providenciales</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### St. Thomas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Caribbean" data-country="U.S. Virgin Islands"><td>The Westin St. Thomas Beach Resort &amp; Spa</td><td>St. Thomas</td><td>THC</td><td>—</td></tr>
</tbody></table>

## Central & South America

### Argentina

#### St. John

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Alvear Palace Hotel</td><td>Buenos Aires, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Arakur Ushuaia Resort &amp; Spa</td><td>Ushuaia, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Awasi Iguazu</td><td>Puerto Iguazu, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Awasi Mendoza</td><td>Luján de Cuyo, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Faena Buenos Aires</td><td>Buenos Aires, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Four Seasons Hotel Buenos Aires</td><td>Buenos Aires, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Gran Melia Iguazu</td><td>Puerto Iguazú, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Llao Llao Resort, Golf &amp; Spa</td><td>San Carlos de Bariloche, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Palacio Duhau - Park Hyatt Buenos Aires</td><td>Buenos Aires, St. John</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>The Vines Resort &amp; Spa</td><td>Tunuyan, St. John</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Buenos Aires

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>Casa Lucia, member of Melia Collection</td><td>Buenos Aires</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>NH Collection Buenos Aires Jousten</td><td>Buenos Aires</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Argentina"><td>SLS Puerto Madero</td><td>Buenos Aires</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Belize

#### Cayo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize"><td>Ka&#x27;ana Resort</td><td>Cayo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Placencia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize"><td>Itzana Resort &amp; Residences</td><td>Placencia</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### San Pedro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Belize"><td>Alaia Belize, Autograph Collection</td><td>San Pedro</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Brazil

#### San Pedro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Awasi Santa Catarina</td><td>Governador Celso Ramos, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Copacabana Palace, A Belmond Hotel, Rio de Janeiro</td><td>Rio de Janeiro, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Emiliano Rio</td><td>Rio de Janeiro, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Emiliano Sao Paulo</td><td>São Paulo, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Fairmont Rio de Janeiro Copacabana</td><td>Copacabana, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Hotel Fasano Angra dos Reis</td><td>Angra dos Reis, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Hotel Fasano Rio De Janeiro</td><td>Rio de Janeiro, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Hotel Fasano Sao Paulo</td><td>São Paulo, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Hotel Unique</td><td>São Paulo, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Hotel das Cataratas, A Belmond Hotel, Iguassu Falls</td><td>Iguassu Falls, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Palacio Tangara, Oetker Hotels</td><td>São Paulo, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Pulso Hotel</td><td>São Paulo, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Brazil"><td>Rosewood Sao Paulo</td><td>São Paulo, San Pedro</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Chile

#### San Pedro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>Mandarin Oriental, Santiago</td><td>Santiago, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>Nayara Alto Atacama</td><td>San Pedro de Atacama, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>The Ritz-Carlton, Santiago</td><td>Santiago, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>Tierra Patagonia, Beckons</td><td>Torres del Paine, San Pedro</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>W Santiago</td><td>Santiago, San Pedro</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Easter Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Chile"><td>Nayara Hangaroa</td><td>Easter Island</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Colombia

#### Easter Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Casa San Agustin</td><td>Cartagena, Easter Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Four Seasons Hotel Bogota</td><td>Bogotá, Easter Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Four Seasons Hotel Casa Medina Bogota</td><td>Bogotá, Easter Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Hotel Las Islas</td><td>Cartagena, Easter Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Sofitel Baru Cartagena Beach Resort</td><td>Cartagena, Easter Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Sofitel Legend Santa Clara Cartagena</td><td>Cartagena, Easter Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>W Bogota Hotel</td><td>Bogotá, Easter Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cartagena de Indias

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Colombia"><td>Capellan de Getsemani</td><td>Cartagena de Indias</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Costa Rica

#### Cartagena de Indias

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>El Silencio Lodge and Spa Costa Rica</td><td>Bajos del Toro, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Four Seasons Resort Peninsula Papagayo, Costa Rica</td><td>Peninsula Papagayo, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Hacienda AltaGracia, Auberge Collection</td><td>Pérez Zeledón, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nayara Gardens</td><td>La Fortuna, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nayara Springs</td><td>La Fortuna, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nayara Tented Camp</td><td>La Fortuna, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nekajui, a Ritz-Carlton Reserve Residences</td><td>Liberia, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Nekajui, a Ritz-Carlton Reserve</td><td>Liberia, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Waldorf Astoria Costa Rica Punta Cacique</td><td>Guanacaste, Cartagena de Indias</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Carrillo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>El Mangroove Autograph Collection</td><td>Carrillo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### La Fortuna

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Amor Arenal</td><td>La Fortuna</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Manuel Antonio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Los Altos Resort</td><td>Manuel Antonio</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Peninsula Papagayo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Andaz Peninsula Papagayo Resort, Costa Rica</td><td>Peninsula Papagayo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Puerto Jimenez

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Botanika Osa Peninsula Costa Rica Resort, Curio Collection by Hilton</td><td>Puerto Jimenez</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### San Jose

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>Gran Hotel Costa Rica, Curio Collection by Hilton</td><td>San Jose</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Tamarindo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Costa Rica"><td>JW Marriott Guanacaste</td><td>Tamarindo</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Ecuador

#### Tamarindo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Ecuador"><td>Casa Gangotena</td><td>Quito, Tamarindo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Ecuador"><td>Finch Bay Galapagos Hotel</td><td>Puerto Ayora, Tamarindo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Ecuador"><td>Mashpi Lodge</td><td>Pacto, Tamarindo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Guayaquil

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Ecuador"><td>Hotel del Parque</td><td>Guayaquil</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Puerto Baquerizo Moreno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Ecuador"><td>Hotel Indigo Galapagos</td><td>Puerto Baquerizo Moreno</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Nicaragua

#### Puerto Baquerizo Moreno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Nicaragua"><td>Rancho Santana</td><td>Tola, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Panama

#### Puerto Baquerizo Moreno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>Hotel La Compania, Panama</td><td>Panama City, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>Hotel la Compania del Valle</td><td>Panama City, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>Nayara Bocas del Toro</td><td>Bocas del Toro, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>Sofitel Legend Casco Viejo, Panama</td><td>Panama City, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>The Santa Maria Hotel, A Luxury Collection &amp; Golf Resort</td><td>Panama City, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>W Panama</td><td>Panama City, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Panama"><td>Waldorf Astoria Panama</td><td>Panama City, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Peru

#### Puerto Baquerizo Moreno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Miraflores Park, A Belmond Hotel, Lima</td><td>Lima, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Palacio Nazarenas, A Belmond Hotel, Cusco</td><td>Cusco, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Palacio del Inka, a Luxury Collection Hotel, Cusco</td><td>Cusco, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Rio Sagrado, A Belmond Hotel, Sacred Valley</td><td>Urubamba, Puerto Baquerizo Moreno</td><td>FHR</td><td><a href="https://www.youtube.com/watch?v=ZsNwOFKryvw">Video</a></td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Tambo del Inka, a Luxury Collection Resort &amp; Spa, Valle Sagrado</td><td>Urubamba, Puerto Baquerizo Moreno</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lima

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>JW Marriott Lima</td><td>Lima</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Swissotel Lima</td><td>Lima</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Miraflores

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Peru"><td>Real Intercontinental Lima Miraflores</td><td>Miraflores</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uruguay

#### Miraflores

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Uruguay"><td>Hotel Fasano Punta del Este</td><td>Punta del Este, Miraflores</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montevideo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Central &amp; South America" data-country="Uruguay"><td>Sofitel Montevideo Casino Carasco &amp; Spa</td><td>Montevideo</td><td>THC</td><td>—</td></tr>
</tbody></table>

## Europe

### Austria

#### Grossarl

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>DAS EDELWEISS Salzburg Mountain Resort</td><td>Grossarl</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hof bei Salzburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Rosewood Schloss Fuschl</td><td>Hof bei Salzburg</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kitzbuehel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Tennerhof Gourmet &amp; Spa de Charme Hotel</td><td>Kitzbuehel</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lech

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Burg Vital Resort</td><td>Lech</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Salzburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Goldener Hirsch, a Luxury Collection Hotel, Salzburg</td><td>Salzburg</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Sacher Salzburg</td><td>Salzburg</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Stein</td><td>Salzburg</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Seefeld

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Alpin Resort Sacher Seefeld–Tirol</td><td>Seefeld</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### St. Anton am Arlberg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Tannenhof</td><td>St. Anton am Arlberg</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Velden am Woerthersee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Falkensteiner Schlosshotel Velden</td><td>Velden am Woerthersee</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vienna

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Almanac Palais Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Anantara Palais Hansen Vienna Hotel</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hilton Vienna Plaza</td><td>Vienna</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Imperial, a Luxury Collection Hotel, Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Sacher Wien, Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hotel Sans Souci Wien</td><td>Vienna</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Hyatt Regency Vienna</td><td>Vienna</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Mandarin Oriental, Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Park Hyatt Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>Rosewood Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>SO/ Vienna</td><td>Vienna</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>The Amauris Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Austria"><td>The Ritz-Carlton, Vienna</td><td>Vienna</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Azerbaijan

#### Baku

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Azerbaijan"><td>Four Seasons Hotel Baku, Azerbaijan</td><td>Baku</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Belgium

#### Antwerp

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Botanic Sanctuary Antwerp</td><td>Antwerp</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Brussels

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Corinthia Grand Hotel Astoria</td><td>Brussels</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Hotel Amigo, a Rocco Forte hotel</td><td>Brussels</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>NH Collection Brussels Grand Sablon</td><td>Brussels</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>Steigenberger Icon Wiltcher&#x27;s, Brussels</td><td>Brussels</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>The Dominican</td><td>Brussels</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>The Hoxton Brussels</td><td>Brussels</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Gent

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Belgium"><td>NH Collection Gent</td><td>Gent</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Bulgaria

#### Sofia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Bulgaria"><td>InterContinental Sofia</td><td>Sofia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Croatia

#### Bale

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Meneghetti Wine Hotel and Winery</td><td>Bale</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dubrovnik

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Hilton Imperial Dubrovnik</td><td>Dubrovnik</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Rixos Premium Dubrovnik</td><td>Dubrovnik</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Sun Gardens Dubrovnik</td><td>Dubrovnik</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Villa Dubrovnik</td><td>Dubrovnik</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hvar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Palace Elisabeth, Hvar Hotel</td><td>Hvar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Opatija

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Keight Hotel Opatija, Curio Collection by Hilton</td><td>Opatija</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Rijeka

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Hilton Rijeka Costabella Beach Resort &amp; Spa</td><td>Rijeka</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Rovinj

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Grand Park Hotel Rovinj</td><td>Rovinj</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Split

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Hotel Ambasador</td><td>Split</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Le Meridien Lav Split</td><td>Split</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Radisson Blu Resort &amp; Spa, Split</td><td>Split</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Stari Grad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Maslina Resort</td><td>Stari Grad</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Zadar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Hyatt Regency Zadar</td><td>Zadar</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Zagreb

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Canopy by Hilton Zagreb</td><td>Zagreb</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Žman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Croatia"><td>Villa Nai 3.3</td><td>Žman</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Cyprus

#### Limassol

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Cyprus"><td>Parklane, a Luxury Collection Resort &amp; Spa, Limassol</td><td>Limassol</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Neo Chorio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Cyprus"><td>Anassa</td><td>Neo Chorio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Czech Republic

#### Prague

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Almanac X Alcron Prague</td><td>Prague</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Andaz Prague</td><td>Prague</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Augustine Hotel, Prague</td><td>Prague</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Fairmont Golden Prague hotel</td><td>Prague</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Four Seasons Hotel Prague</td><td>Prague</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Hilton Prague Old Town</td><td>Prague</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>Mandarin Oriental, Prague</td><td>Prague</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>The Grand Mark Prague</td><td>Prague</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Czech Republic"><td>W Prague</td><td>Prague</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Czechia

#### Prague

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Czechia"><td>NH Collection Prague Carlo IV</td><td>Prague</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Denmark

#### Copenhagen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>1 Hotel Copenhagen</td><td>Copenhagen</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>25hours Hotel Paper Island</td><td>Copenhagen</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>NH Collection Copenhagen</td><td>Copenhagen</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>Nobis Hotel Copenhagen</td><td>Copenhagen</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>Villa Copenhagen</td><td>Copenhagen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>d&#x27;Angleterre, Copenhagen</td><td>Copenhagen</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hellerup

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Denmark"><td>Park Lane Copenhagen</td><td>Hellerup</td><td>THC</td><td>—</td></tr>
</tbody></table>

### England

#### Ascot

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Coworth Park</td><td>Ascot</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bath

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Gainsborough Bath Spa</td><td>Bath</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Royal Crescent Hotel &amp; Spa</td><td>Bath</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Berkshire

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Cliveden House</td><td>Berkshire</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Broadway

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Dormy House Hotel &amp; Spa</td><td>Broadway</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Foxhill Manor</td><td>Broadway</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cambridge

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>University Arms Hotel, an Autograph Collection, Cambridge</td><td>Cambridge</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Colerne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Lucknam Park, Emblems Collection</td><td>Colerne</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cowley

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Cowley Manor Experimental</td><td>Cowley</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hertfordshire

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Grove</td><td>Hertfordshire</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hook

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Four Seasons Hotel Hampshire</td><td>Hook</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Iver

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Langley, a Luxury Collection Hotel, Buckinghamshire</td><td>Iver</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Leatherhead

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Beaverbrook</td><td>Leatherhead</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### London

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>1 Hotel Mayfair</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>45 Park Lane</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Broadwick Soho</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Brown&#x27;s Hotel, a Rocco Forte hotel</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Bvlgari Hotel London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Claridge&#x27;s</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Corinthia London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Four Seasons Hotel London at Park Lane</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Four Seasons Hotel London at Tower Bridge</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Grosvenor House Suites</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Ham Yard Hotel</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Hotel Cafe Royal</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Jumeirah Carlton Tower</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>L&#x27;oscar London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Mandarin Oriental Hyde Park, London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Mandarin Oriental Mayfair, London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>NoMad London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Nobu Hotel London Portman Square</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Pan Pacific London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Park Hyatt London River Thames</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Raffles London at the OWO</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Rosewood London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Shangri-La The Shard, London</td><td>London</td><td>FHR</td><td><a href="https://www.youtube.com/watch?v=qTc6jlWKKzU">Video</a></td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Six Senses London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Beaumont Mayfair</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Berkeley</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Biltmore Mayfair</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Cadogan, A Belmond Hotel, London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Chancery Rosewood</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Connaught</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Dorchester</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Emory</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Goring</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Lanesborough, Oetker Hotels</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Langham, London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The London EDITION</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Londoner</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Peninsula London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Ritz London</td><td>London</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>The Savoy London, A Fairmont Managed Hotel</td><td>London</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### New Milton

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Chewton Glen Hotel &amp; Spa</td><td>New Milton</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Oxfordshire

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Estelle Manor</td><td>Oxfordshire</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ripon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="England"><td>Grantley Hall</td><td>Ripon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Finland

#### Helsinki

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Finland"><td>Hotel Kamp</td><td>Helsinki</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Finland"><td>Hotel Lilla Roberts</td><td>Helsinki</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Finland"><td>Hotel U14 - Autograph Collection</td><td>Helsinki</td><td>THC</td><td><a href="https://visitkarma.com/p/hotel-u14-helsinki-a-marriott-autograph-collection-gem-by-market-square/">Blog</a> · <a href="https://www.youtube.com/watch?v=TOqExQg6Was">Video</a></td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Finland"><td>NH Collection Helsinki Grand Hansa</td><td>Helsinki</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Finland"><td>Waldorf Astoria Helsinki</td><td>Helsinki</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### France

#### Antibes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel du Cap-Eden-Roc, Oetker Hotels</td><td>Antibes</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Villa Mirae by Inwood Hotels</td><td>Antibes</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Audrieu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Chateau d&#x27;Audrieu</td><td>Audrieu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Avignon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Mirande</td><td>Avignon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Biarritz

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel du Palais Biarritz</td><td>Biarritz</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Regina Experimental Biarritz</td><td>Biarritz</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Bonnieux

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Capelongue, a Beaumier Hotel</td><td>Bonnieux</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bordeaux

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Burdigala by Inwood Hotels</td><td>Bordeaux</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>FirstName Bordeaux</td><td>Bordeaux</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Bordeaux - Le Grand Hotel</td><td>Bordeaux</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Mondrian Bordeaux Les Carmes</td><td>Bordeaux</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Yndo Hotel</td><td>Bordeaux</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Cannes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Canopy by Hilton Cannes</td><td>Cannes</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Carlton Cannes, a Regent Hotel</td><td>Cannes</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Five Seas Hotel Cannes</td><td>Cannes</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Barriere Le Majestic Cannes</td><td>Cannes</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Le Gray D&#x27;Albion Cannes</td><td>Cannes</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Martinez</td><td>Cannes</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>JW Marriott Cannes</td><td>Cannes</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Mondrian Cannes</td><td>Cannes</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Cassis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Les Roches Blanches Cassis</td><td>Cassis</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cernay-la-Ville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Abbaye des Vaux-de-Cernay</td><td>Cernay-la-Ville</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Champillon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Royal Champagne Hotel &amp; Spa</td><td>Champillon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Chantilly

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Auberge du Jeu de Paume</td><td>Chantilly</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cheverny

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Les Sources de Cheverny</td><td>Cheverny</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cognac

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Chais Monnet &amp; Spa</td><td>Cognac</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Courchevel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Aman Le Melezin</td><td>Courchevel</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cheval Blanc Courchevel</td><td>Courchevel</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Fouquet&#x27;s Courchevel</td><td>Courchevel</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Le K2 Palace</td><td>Courchevel</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>L&#x27;Apogee Courchevel, Oetker Hotels</td><td>Courchevel</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Rosewood Courchevel Le Jardin Alpin</td><td>Courchevel</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Deauville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Barriere Le Normandy</td><td>Deauville</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dinard

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Barriere Le Grand Hotel Dinard</td><td>Dinard</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Barriere Le Grand Hotel Dinard</td><td>Dinard</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Gargas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Coquillade Provence</td><td>Gargas</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Gilly-lès-Cîteaux

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Les Sources de Vougeot</td><td>Gilly-lès-Cîteaux</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Gordes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Airelles La Bastide, Gordes</td><td>Gordes</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Grimaud

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>COMO Le Beauvallon</td><td>Grimaud</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Guainville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine de Primard</td><td>Guainville</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Honfleur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Ferme Saint Simeon</td><td>Honfleur</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Jouy-en-Josas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Dolce by Wyndham Versailles</td><td>Jouy-en-Josas</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### La Chapelle-en-Serval

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Chantilly Chateau Mont Royal</td><td>La Chapelle-en-Serval</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### La Croix Valmer

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Lily of the Valley</td><td>La Croix Valmer</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lauris

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine de Fontenille</td><td>Lauris</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Le Puy-Sainte-Réparade

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Villa La Coste</td><td>Le Puy-Sainte-Réparade</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Les Baux de Provence

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine de Manville</td><td>Les Baux de Provence</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Levernois

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hostellerie de Levernois</td><td>Levernois</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lyon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Boscolo Hôtel &amp; Spa Lyon</td><td>Lyon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Lyon Hotel Dieu</td><td>Lyon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Villa Maia Lyon</td><td>Lyon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Marseille

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Marseille-Hotel Dieu</td><td>Marseille</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Martillac

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Les Sources de Caudalie</td><td>Martillac</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Massignac

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine des Etangs, Auberge Collection</td><td>Massignac</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Megeve

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Four Seasons Resort Megeve</td><td>Megeve</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Les Fermes De Marie</td><td>Megeve</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nice

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Anantara Plaza Nice Hotel</td><td>Nice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Palais de la Mediterranee</td><td>Nice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel du Couvent, a Luxury Collection Hotel, Nice</td><td>Nice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Negresco</td><td>Nice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Albar - Le Victoria</td><td>Nice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Radisson Blu Hotel Nice</td><td>Nice</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nimes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Albar - L&#x27;Imperator</td><td>Nimes</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Paris

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Brach Paris - Evok Collection</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Bvlgari Hotel Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Canopy by Hilton Paris Eiffel Tower</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Castille Paris</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Chateau des Fleurs</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cheval Blanc Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Experimental Marais</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Fauchon L&#x27;Hotel Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Fouquet&#x27;s Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Four Seasons Hotel George V</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hilton Paris Opera</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Alfred Sommier</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Bel Ami</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Bowmann</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Dame des Arts</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Elysia by Inwood Hotels</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Florida Paris</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Hana</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Lancaster</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Pavillon de la Reine</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Plaza Athenee Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Vernet Champs Elysees</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel de Crillon, A Rosewood Hotel</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>InterContinental Paris Le Grand</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>J.K. Place Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Kimpton St Honore Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Demeure Montaigne</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Fantaisie</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Reserve Paris Hotel and Spa</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Bristol Paris, Oetker Hotels</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Meurice</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Pavillon Faubourg Saint-Germain</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Roch Hotel and Spa</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Le Royal Monceau Raffles Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Les Bains</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Albar - Le Pont-Neuf</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Albar - Le Vendome</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Astor Paris, Curio Collection by Hilton</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Barriere Vendome</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Colbert, Member of Melia Collection</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Maison Delano Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Mandarin Oriental Lutetia, Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Mandarin Oriental, Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Molitor Hotel &amp; Spa Paris MGallery Collection</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Nolinski Paris - Evok Collection</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Park Hyatt Paris-Vendome</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Prince de Galles, a Luxury Collection Hotel, Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Ritz Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>SAX Paris, LXR Hotels &amp; Resorts</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>SO/ Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Saint James Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>San Regis</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Shangri-La Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Le Scribe Paris Opera</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Paris Arc de Triomphe</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Paris Baltimore Tour Eiffel</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Paris Le Faubourg</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>The Hoxton, Paris</td><td>Paris</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>The Peninsula Paris</td><td>Paris</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Porto-Vecchio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Casadelmar</td><td>Porto-Vecchio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Puligny-Montrachet

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>COMO Le Montrachet</td><td>Puligny-Montrachet</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ramatuelle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Reserve Ramatuelle hotel spa &amp; villas</td><td>Ramatuelle</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Villa Marie Saint Tropez</td><td>Ramatuelle</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Reugny

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Chateau Louise de La Valliere</td><td>Reugny</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Roquebrune-Cap-Martin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Monte-Carlo Beach</td><td>Roquebrune-Cap-Martin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>The Maybourne Riviera</td><td>Roquebrune-Cap-Martin</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Saint Paul de Vence

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Domaine du Mas de Pierre</td><td>Saint Paul de Vence</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Saint-Gervais-les-Bains

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Armancette</td><td>Saint-Gervais-les-Bains</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Saint-Jean-Cap-Ferrat

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Grand-Hotel du Cap-Ferrat, A Four Seasons Hotel</td><td>Saint-Jean-Cap-Ferrat</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Royal-Riviera</td><td>Saint-Jean-Cap-Ferrat</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Saint-Tropez

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Airelles Château de La Messardière, Saint Tropez</td><td>Saint-Tropez</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cheval Blanc St-Tropez</td><td>Saint-Tropez</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel de Paris Saint-Tropez</td><td>Saint-Tropez</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>La Tartane St Tropez</td><td>Saint-Tropez</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Strasbourg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Sofitel Strasbourg Grande Ile</td><td>Strasbourg</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Tourrettes

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Terre Blanche Hotel Spa Golf Resort</td><td>Tourrettes</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Trouville Sur Mer

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cures Marines Hotel &amp; Spa Trouville MGallery Collection</td><td>Trouville Sur Mer</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Val d'Isère

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Airelles Val d&#x27;Isere</td><td>Val d&#x27;Isère</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vence

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Chateau Saint-Martin &amp; Spa, Oetker Hotels</td><td>Vence</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Versailles

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Airelles Le Grand Contrôle, Château de Versailles</td><td>Versailles</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Waldorf Astoria Versailles - Trianon Palace</td><td>Versailles</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Èze

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Cap Estel</td><td>Èze</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Chateau de La Chevre d&#x27;Or</td><td>Èze</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Évian-les-Bains

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="France"><td>Hotel Royal - Evian Resort</td><td>Évian-les-Bains</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Germany

#### Baden-Baden

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Brenners Park-Hotel &amp; Spa, Oetker Hotels</td><td>Baden-Baden</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Berchtesgaden

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Kempinski Hotel Berchtesgaden</td><td>Berchtesgaden</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Berlin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Das Stue</td><td>Berlin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Grand Hyatt Berlin</td><td>Berlin</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hilton Berlin</td><td>Berlin</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel Adlon Kempinski Berlin</td><td>Berlin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel de Rome</td><td>Berlin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>InterContinental Berlin</td><td>Berlin</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Hoxton, Charlottenburg</td><td>Berlin</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Mandala Hotel</td><td>Berlin</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Ritz-Carlton, Berlin</td><td>Berlin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Waldorf Astoria Berlin</td><td>Berlin</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cologne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Excelsior Hotel Ernst</td><td>Cologne</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dresden

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel Taschenbergpalais Kempinski Dresden</td><td>Dresden</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Düsseldorf

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Breidenbacher Hof</td><td>Düsseldorf</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Elmau

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Schloss Elmau Luxury Spa Retreat &amp; Cultural Hideaway</td><td>Elmau</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Frankfurt

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Avani Frankfurt City</td><td>Frankfurt</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>JW Marriott Hotel Frankfurt</td><td>Frankfurt</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>NH Collection Frankfurt Spin Tower</td><td>Frankfurt</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Sofitel Frankfurt Opera</td><td>Frankfurt</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Steigenberger Icon Frankfurter Hof</td><td>Frankfurt</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Florentin by Althoff Collection</td><td>Frankfurt</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Frankfurt am Main

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Kimpton Main Frankfurt</td><td>Frankfurt am Main</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Hamburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Conrad Hamburg</td><td>Hamburg</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Fairmont Hotel Vier Jahreszeiten</td><td>Hamburg</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Fontenay Hamburg</td><td>Hamburg</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kreuth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Spa &amp; Resort Bachmair Weissach</td><td>Kreuth</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Munich

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Andaz Munich Schwabinger Tor</td><td>Munich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Cortiina Hotel</td><td>Munich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel Bayerischer Hof, Munich</td><td>Munich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel Munchen Palace</td><td>Munich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Hotel Vier Jahreszeiten Kempinski Munich</td><td>Munich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Koenigshof, a Luxury Collection Hotel, Munich</td><td>Munich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Louis Hotel</td><td>Munich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Mandarin Oriental, Munich</td><td>Munich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>NH Collection Munchen Bavaria</td><td>Munich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Rosewood Munich</td><td>Munich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Sofitel Munich Bayerpost</td><td>Munich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Charles Hotel, a Rocco Forte hotel</td><td>Munich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Dean Munich – Autograph Collection</td><td>Munich</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Rottach-Egern

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Althoff Seehotel Ueberfahrt</td><td>Rottach-Egern</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Weissenhaus

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Weissenhaus Private Nature Luxury Resort</td><td>Weissenhaus</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Wolfsburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>The Ritz-Carlton, Wolfsburg</td><td>Wolfsburg</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Übersee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Germany"><td>Chiemgauhof - Lakeside Retreat</td><td>Übersee</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Greece

#### Agioi Apostoloi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Noruz Chania, Autograph Collection</td><td>Agioi Apostoloi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Agios Nikolaos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>NIKO Seaside Resort Crete MGALLERY</td><td>Agios Nikolaos</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Athens

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>91 Athens Riviera</td><td>Athens</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Academias Hotel, Autograph Collection</td><td>Athens</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Ace Hotel &amp; Swim Club Athens</td><td>Athens</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Athens Capital Hotel – MGallery Collection</td><td>Athens</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Athens Capital Suites - MGallery Collection</td><td>Athens</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Four Seasons Astir Palace Hotel Athens</td><td>Athens</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Grecotel The Dolli at Acropolis</td><td>Athens</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Hotel Grande Bretagne, a Luxury Collection Hotel, Athens</td><td>Athens</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>King George, a Luxury Collection Hotel, Athens</td><td>Athens</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>NEW Hotel</td><td>Athens</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>NJV Athens Plaza</td><td>Athens</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>One&amp;Only Aesthesis</td><td>Athens</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Chania

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Zeen Chania, a Luxury Collection Resort, Crete</td><td>Chania</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>JW Marriott Crete Resort &amp; Spa</td><td>Chania</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Corfu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Angsana Corfu</td><td>Corfu</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Miramare, a Luxury Collection Resort, Corfu</td><td>Corfu</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes of Corfu, Autograph Collection</td><td>Corfu</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Elounda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Aulus Elounda Resort, Curio Collection by Hilton</td><td>Elounda</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes of Elounda, Autograph Collection</td><td>Elounda</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Phaea Blue, Elounda, Crete</td><td>Elounda</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Emionida

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Amanzoe</td><td>Emionida</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Fira

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Cosmopolitan Suites</td><td>Fira</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Garden</td><td>Fira</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Folegandros

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Gundari</td><td>Folegandros</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Imerovigli

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Andronis Concept</td><td>Imerovigli</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Chromata Santorini</td><td>Imerovigli</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kamari

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Sandblu Santorini, LXR Hotels &amp; Resorts</td><td>Kamari</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Kefalonia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Eliamos Villas Hotel &amp; Spa</td><td>Kefalonia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Keá Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>One&amp;Only Kea Island</td><td>Keá Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lardos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Aulus Lindos Rhodes Resort, Curio Collection by Hilton</td><td>Lardos</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Magouliana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Manna</td><td>Magouliana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Megalochori

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Vedema, a Luxury Collection Resort, Santorini</td><td>Megalochori</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Messinia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>The Romanos, a Luxury Collection Resort, Costa Navarino</td><td>Messinia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Milos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes White Coast Milos</td><td>Milos</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mykonos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Bill &amp; Coo Mykonos</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Cali Mykonos</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Deos Mykonos Hotel</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Kalesma Mykonos</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Mykonos</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian Ambassador Relais &amp; Chateaux Hotel</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian Korali Hotel</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian O a Member of Design Hotels</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Myconian Villa Collection</td><td>Mykonos</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mykonos Blanc Hotel</td><td>Mykonos</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mykonos Riviera Hotel &amp; Spa</td><td>Mykonos</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Nomad Mykonos</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>OMEON Mykonos</td><td>Mykonos</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Santa Marina, a Luxury Collection Resort, Mykonos</td><td>Mykonos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Semeli Coast Mykonos, Curio Collection by Hilton</td><td>Mykonos</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Naoussa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Avant Mar</td><td>Naoussa</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Cosme, a Luxury Collection Resort, Paros</td><td>Naoussa</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nea Roda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Avaton Luxury Beach Resort</td><td>Nea Roda</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nikiti

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>The Danai</td><td>Nikiti</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Oia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Andronis Arcadia</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Andronis Luxury Suites</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Canaves Ena</td><td>Oia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Canaves Epitome</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Canaves Oia Suites</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Novos Santorini, Autograph Collection</td><td>Oia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Santorini - Gea House</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Katikies Santorini</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mystique, a Luxury Collection Hotel, Santorini</td><td>Oia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Santo Mine Oia Suites</td><td>Oia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ouranoupolis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Eagles Villas</td><td>Ouranoupolis</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Patmos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Patmos Aktis, a Luxury Collection Resort &amp; Spa, Greece</td><td>Patmos</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pylos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Mandarin Oriental, Costa Navarino</td><td>Pylos</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Rethymnon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Caramel A Grecotel Resort to live, Crete</td><td>Rethymnon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>GRECOTEL LUXME WHITE</td><td>Rethymnon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>The Royal Senses Resort Crete, Curio Collection by Hilton</td><td>Rethymnon</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Santorini

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Kivotos Santorini</td><td>Santorini</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Magma Resort Santorini, part of The Unbound Collection by Hyatt</td><td>Santorini</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>NOUS Santorini</td><td>Santorini</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Sea Breeze Santorini Beach Resort, Curio Collection by Hilton</td><td>Santorini</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Thira

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Grace Hotel, Auberge Collection</td><td>Thira</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tinos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Odera. Tinos, Autograph Collection</td><td>Tinos</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vouliagmeni

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Divani Apollon Palace &amp; Thalasso</td><td>Vouliagmeni</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Zakynthos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Domes Aulus Zante, Autograph Collection</td><td>Zakynthos</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Lesante Cape</td><td>Zakynthos</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Greece"><td>Porto Zante Villas &amp; Spa, Zakynthos</td><td>Zakynthos</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Hungary

#### Budapest

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Al Habtoor Palace Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Anantara New York Palace Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Aria Hotel Budapest by Library Hotel Collection</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Dorothea Hotel, Budapest, Autograph Collection</td><td>Budapest</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Four Seasons Hotel Gresham Palace Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Kempinski Corvinus Budapest</td><td>Budapest</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Kimpton BEM Budapest</td><td>Budapest</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Matild Palace, a Luxury Collection Hotel, Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Mystery Hotel Budapest</td><td>Budapest</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>Parisi Udvar Hotel Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>The St. Regis Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Hungary"><td>W Budapest</td><td>Budapest</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Iceland

#### Reykjavik

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Iceland"><td>Iceland Parliament Hotel, Curio Collection by Hilton</td><td>Reykjavik</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Iceland"><td>The EDITION Reykjavik</td><td>Reykjavik</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Ireland

#### Adare

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Adare Manor</td><td>Adare</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ballyfin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Ballyfin Demesne</td><td>Ballyfin</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cashel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Cashel Palace Hotel</td><td>Cashel</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Cong

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Ashford Castle</td><td>Cong</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cork City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Hayfield Manor</td><td>Cork City</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Doonbeg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Trump International Golf Links &amp; Hotel Ireland, Doonbeg</td><td>Doonbeg</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dublin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Anantara The Marker Dublin Hotel</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Conrad Dublin</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Dylan Hotel Dublin</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>InterContinental Dublin</td><td>Dublin</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The College Green Hotel Dublin</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Merrion Dublin</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Shelbourne Dublin</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Westbury</td><td>Dublin</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Galway

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Glenlo Abbey Hotel &amp; Estate</td><td>Galway</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Kenmare

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Sheen Falls Lodge</td><td>Kenmare</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kilkenny

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Mount Juliet Estate</td><td>Kilkenny</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Killarney

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Europe Hotel &amp; Resort</td><td>Killarney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The Killarney Park Hotel</td><td>Killarney</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Maynooth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Carton House, A Fairmont Managed Hotel</td><td>Maynooth</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Newmarket-on-Fergus

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Dromoland Castle</td><td>Newmarket-on-Fergus</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Straffan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>The K Club</td><td>Straffan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Waterford

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Ireland"><td>Cliff House Hotel</td><td>Waterford</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Italy

#### Alassio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa della Pergola</td><td>Alassio</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Alpe di Siusi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>COMO Alpina Dolomites</td><td>Alpe di Siusi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Amalfi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Anantara Convento di Amalfi Grand Hotel</td><td>Amalfi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Miramalfi</td><td>Amalfi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Santa Caterina, Amalfi</td><td>Amalfi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Anacapri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Caesar Augustus</td><td>Anacapri</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Arezzo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il Borro Toscana</td><td>Arezzo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Arzachena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>W Sardinia - Poltu Quatu</td><td>Arzachena</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Avelengo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Miramonti Boutique Hotel</td><td>Avelengo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Baja Sardinia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>7Pines Resort Sardinia</td><td>Baja Sardinia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bellagio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Villa Serbelloni</td><td>Bellagio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bernalda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Margherita</td><td>Bernalda</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Blevio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Mandarin Oriental, Lago di Como</td><td>Blevio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bologna

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Corona d&#x27;Oro 1890</td><td>Bologna</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Grand Hotel Majestic già Baglioni</td><td>Bologna</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bressanone

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Forestis</td><td>Bressanone</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Brindisi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo Egnazia</td><td>Brindisi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cadenabbia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Lake Como EDITION</td><td>Cadenabbia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cagliari

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Tirso Cagliari MGallery</td><td>Cagliari</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Candeli

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa La Massa</td><td>Candeli</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cannigione

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Aethos Sardinia</td><td>Cannigione</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Capalbio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Locanda Rossa</td><td>Capalbio</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Capri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Capri Tiberio Palace</td><td>Capri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Quisisana</td><td>Capri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel La Palma, Oetker Hotels</td><td>Capri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>J.K. Place Capri</td><td>Capri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Jumeirah Capri Palace</td><td>Capri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Pazziella, a Luxury Collection Hotel, Capri</td><td>Capri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Punta Tragara</td><td>Capri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Marina Capri Hotel &amp; Spa</td><td>Capri</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Casole d'Elsa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castello di Casole, A Belmond Hotel, Tuscany</td><td>Casole d&#x27;Elsa</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Castelnuovo Berardenga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo San Felice Resort</td><td>Castelnuovo Berardenga</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Club House</td><td>Castelnuovo Berardenga</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Castiglione della Pescaia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>L&#x27;Andana</td><td>Castiglione della Pescaia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Catania

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Relais &amp; Chateaux Monaci delle Terre Nere</td><td>Catania</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cernobbio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa D&#x27;Este</td><td>Cernobbio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cerretto Langhe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa di Langa</td><td>Cerretto Langhe</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cima di Porlezza

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Aria Retreat &amp; SPA</td><td>Cima di Porlezza</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cinigiano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castello di Vicarello</td><td>Cinigiano</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Como

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hilton Lake Como</td><td>Como</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo San Gottardo Lake Como, Radisson Collection Hotel</td><td>Como</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Venezia</td><td>Como</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cortona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa di Piazzano</td><td>Cortona</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Courmayeur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Le Massif</td><td>Courmayeur</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Domus de Maria

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Conrad Chia Laguna Sardinia</td><td>Domus de Maria</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Duino Aurisina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Tivoli Portopiccolo Sistiana Wellness Resort &amp; Spa</td><td>Duino Aurisina</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Erbusco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>L&#x27;Albereta Relais &amp; Chateaux</td><td>Erbusco</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Fasano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Masseria Torre Coccaro</td><td>Fasano</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Fiuggi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Fiuggi</td><td>Fiuggi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Florence

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Anglo American Hotel Florence, Curio Collection by Hilton</td><td>Florence</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Collegio alla Querce, Auberge Collection</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Four Seasons Hotel Firenze</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Minerva</td><td>Florence</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Helvetia &amp; Bristol Firenze</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel La Gemma</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Lungarno</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Regency, Firenze</td><td>Florence</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Savoy, a Rocco Forte hotel</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>IL Tornabuoni Hotel</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il Salviatino</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Portinari Salviati</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Porta Rossa Hotel Firenze, Colbert Collection</td><td>Florence</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Portrait Firenze</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>SINA Villa Medici, Autograph Collection</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Place Firenze</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The St. Regis Florence</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Tivoli Palazzo Gaddi</td><td>Florence</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Cora</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa San Michele, A Belmond Hotel, Florence</td><td>Florence</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>W Florence</td><td>Florence</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Follonica

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Sense Experience Resort</td><td>Follonica</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Forio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Botania Relais &amp; Spa</td><td>Forio</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Mezzatorre Hotel &amp; Thermal Spa</td><td>Forio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Forte dei Marmi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Principe Forte dei Marmi</td><td>Forte dei Marmi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Furore

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Furore Grand Hotel</td><td>Furore</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Gardone Riviera

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Fasano</td><td>Gardone Riviera</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Gargnano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Lefay Resort &amp; SPA Lago di Garda</td><td>Gargnano</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lacco Ameno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>San Montano Resort &amp; Spa</td><td>Lacco Ameno</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Lagundo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Avidea</td><td>Lagundo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Lana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Vigilius Mountain Resort</td><td>Lana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lipari

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Therasia Resort Sea &amp; Spa</td><td>Lipari</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lisciano Niccone

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Reschio Hotel</td><td>Lisciano Niccone</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Malcesine

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Val di Sogno</td><td>Malcesine</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Maratea

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Santavenere</td><td>Maratea</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Menaggio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Victoria Concept &amp; Spa</td><td>Menaggio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Merano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castel Fragsburg</td><td>Merano</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Milan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Aethos Milan</td><td>Milan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Armani Hotel Milano</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Bvlgari Hotel Milano</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Baglioni Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Brera, a Luxury Collection Hotel, Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Cipriani Milano</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Excelsior Hotel Gallia, a Luxury Collection Hotel, Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Four Seasons Hotel Milano</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel et de Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Principe di Savoia</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel VIU Milan</td><td>Milan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>ME Milan II Duca</td><td>Milan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Mandarin Oriental, Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NEMI Hotel Milano</td><td>Milan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Cordusio, a Gran Melia Hotel Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Parigi Hotel &amp; Grand Spa, Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Touring Club Milan, a Radisson Collection Hotel</td><td>Milan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Park Hyatt Milano</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Portrait Milano</td><td>Milan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Carlton, Milan</td><td>Milan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Monastero Bormida

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa La Madonna</td><td>Monastero Bormida</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Montaione

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castelfalfi</td><td>Montaione</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montalcino

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castiglion del Bosco, A Rosewood Hotel</td><td>Montalcino</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montignoso

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il Bottaccio, Relais &amp; Châteaux</td><td>Montignoso</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Naples

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Parker&#x27;s</td><td>Naples</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>ROMEO Napoli</td><td>Naples</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>de Bonart Naples, Curio Collection by Hilton</td><td>Naples</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nervi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Capitolo Riviera</td><td>Nervi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Noto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il San Corrado di Noto</td><td>Noto</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Oltretorrente

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Gardena Grodnerhof Hotel &amp; Spa</td><td>Oltretorrente</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Orta San Giulio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Crespi</td><td>Orta San Giulio</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ostuni

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>La Sommita Relais</td><td>Ostuni</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Vista Ostuni</td><td>Ostuni</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Palazzetto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo Santo Pietro</td><td>Palazzetto</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Palermo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Igiea, a Rocco Forte Hotel</td><td>Palermo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Perugia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo dei Conti Resort</td><td>Perugia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pettenasco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Laqua by the Lake</td><td>Pettenasco</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Pinzolo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Lefay Resort &amp; SPA Dolomiti</td><td>Pinzolo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Porto Cervo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Cala di Volpe, a Luxury Collection Hotel, Costa Smeralda</td><td>Porto Cervo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Pitrizza</td><td>Porto Cervo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Porto Ercole

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Il Pellicano</td><td>Porto Ercole</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>La Roqqa</td><td>Porto Ercole</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Porto Rotondo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Sulia House Porto Rotondo, Curio Collection by Hilton</td><td>Porto Rotondo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Portofino

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Splendido Mare, A Belmond Hotel, Portofino</td><td>Portofino</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Splendido, A Belmond Hotel, Portofino</td><td>Portofino</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Portovenere

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Portovenere</td><td>Portovenere</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Positano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Villa Franca</td><td>Positano</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Le Sirenuse</td><td>Positano</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Treville</td><td>Positano</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Praiano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Casa Angelina</td><td>Praiano</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pula

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Forte Village Sardinia - Villa Del Parco &amp; Spa</td><td>Pula</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Punta Ala

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Cala Beach Resort</td><td>Punta Ala</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Quattro Castella

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Relais Roncolo 1888</td><td>Quattro Castella</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Radda in Chianti

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Pieve Aldina</td><td>Radda in Chianti</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Rapallo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Bristol Spa Resort</td><td>Rapallo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ravello

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Caruso, A Belmond Hotel, Amalfi Coast</td><td>Ravello</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Avino</td><td>Ravello</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Riva del Garda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Lido Palace</td><td>Riva del Garda</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Rome

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Aleph Rome Hotel, Curio Collection by Hilton</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Anantara Palazzo Naiadi Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Baglioni Hotel Regina, Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Bvlgari Hotel Roma</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Corinthia Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Elizabeth Unique Hotel</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hassler Roma</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Eden, Dorchester Collection</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Locarno Roma</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Splendide Royal Roma</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Vilon</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel d&#x27;Inghilterra, Starhotels Collezione</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel de Russie, a Rocco Forte hotel</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel de la Ville, a Rocco Forte hotel</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>InterContinental Rome Ambasciatori Palace</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>J.K. Place Roma</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Fori Imperiali</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Roma Giustiniano</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Rome Palazzo Cinquecento</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Orient Express La Minerva</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Ripetta</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Roma</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Talia</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Parco dei Principi Grand Hotel &amp; Spa Roma</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Portrait Roma</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rome Cavalieri, A Waldorf Astoria Hotel</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Six Senses Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Sofitel Rome Villa Borghese</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The First Dolce</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The First Musica</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The First Roma Arte</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Hoxton Rome</td><td>Rome</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Rome EDITION</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The St. Regis Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Umilta 36</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Agrippina, A Gran Melia Hotel, Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>W Rome</td><td>Rome</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### San Cassiano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Aman Rosa Alpina</td><td>San Cassiano</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### San Lorenzo di Sebato

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Castel Badia</td><td>San Lorenzo di Sebato</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### San Teodoro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Baglioni Resort Sardinia</td><td>San Teodoro</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sanremo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Royal Hotel Sanremo</td><td>Sanremo</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Santa Margherita Ligure

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Miramare</td><td>Santa Margherita Ligure</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Savelletri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Masseria Torre Maizza, a Rocco Forte hotel</td><td>Savelletri</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sciacca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Rocco Forte Private Villas</td><td>Sciacca</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Verdura Resort, a Rocco Forte hotel</td><td>Sciacca</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Siena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Continental</td><td>Siena</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Siracusa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Ortea Palace Hotel, Sicily - Autograph Collection</td><td>Siracusa</td><td>THC</td><td><a href="https://www.youtube.com/watch?v=tCRYX0A11C0">Video</a></td></tr>
</tbody></table>

#### Sorrento

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Ara Maris</td><td>Sorrento</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Excelsior Vittoria</td><td>Sorrento</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Paro dei Principi Sorrento</td><td>Sorrento</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Taormina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel San Pietro Taormina</td><td>Taormina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Timeo, A Belmond Hotel, Taormina</td><td>Taormina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Mazzarò Sea Palace</td><td>Taormina</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Taormina</td><td>Taormina</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>San Domenico Palace, Taormina, a Four Seasons Hotel</td><td>Taormina</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Taormina Mare

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Villa Sant&#x27;Andrea, A Belmond Hotel, Taormina Mare</td><td>Taormina Mare</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tavarnelle Val di Pesa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>COMO Castello Del Nero</td><td>Tavarnelle Val di Pesa</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Torino

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Principi di Piemonte UNA Esperienze</td><td>Torino</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Torno

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Il Sereno Hotel Lake Como</td><td>Torno</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Torri del Benaco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Cape of Senses</td><td>Torri del Benaco</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Torrita di Siena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Lupaia</td><td>Torrita di Siena</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tremezzina

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Tremezzo, Lake Como</td><td>Tremezzina</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Venice

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Aman Venice</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Baglioni Hotel Luna</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Ca&#x27; di Dio</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hilton Molino Stucky Venice</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Ai Reali</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Cipriani, A Belmond Hotel, Venice</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hotel Gabrielli Venezia - Starhotels Collezione</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Hyatt Centric Murano Venice</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>IL Palazzo Experimental</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>JW Marriott Venice Resort &amp; Spa</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Londra Palace Venezia</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Murano Villa</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Venice Grand Hotel Palazzo Dei Dogi</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Nolinski Venezia - Evok Collection</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Orient Express Venezia</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Palazzo Venart Luxury Hotel</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>San Clemente Palace</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Sina Centurion Palace</td><td>Venice</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Gritti Palace, a Luxury Collection Hotel, Venice</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The St. Regis Venice</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>The Venice Venice Hotel</td><td>Venice</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Violino d&#x27;Oro Venezia</td><td>Venice</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Verona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>NH Collection Palazzo Verona</td><td>Verona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Vista Verona</td><td>Verona</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Viareggio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Grand Hotel Principe di Piemonte</td><td>Viareggio</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Volterra

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Italy"><td>Borgo Pignano Volterra Tuscany</td><td>Volterra</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Liechtenstein

#### Vaduz

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Liechtenstein"><td>Park Hotel Sonnenhof</td><td>Vaduz</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Malta

#### Floriana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Malta"><td>The Phoenicia-Malta</td><td>Floriana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### San Anton

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Malta"><td>Corinthia Palace Malta</td><td>San Anton</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### St Julian's

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Malta"><td>ME Malta</td><td>St Julian&#x27;s</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Valletta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Malta"><td>Iniala Valletta</td><td>Valletta</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Monaco

#### Monaco

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Columbus Hotel Monte-Carlo, Curio Collection by Hilton</td><td>Monaco</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Monte-Carlo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Fairmont Monte Carlo</td><td>Monte-Carlo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Hotel Hermitage Monte-Carlo</td><td>Monte-Carlo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Hotel Metropole Monte Carlo</td><td>Monte-Carlo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Hotel de Paris Monte-Carlo</td><td>Monte-Carlo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Monaco"><td>Monte-Carlo Bay Hotel &amp; Resort</td><td>Monte-Carlo</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Montenegro

#### Herceg Novi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>One&amp;Only Portonovi</td><td>Herceg Novi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Perast

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>Heritage Grand Perast</td><td>Perast</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Tivat

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>Regent Porto Montenegro</td><td>Tivat</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>SIRO Boka Place</td><td>Tivat</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Montenegro"><td>The Chedi Lustica Bay</td><td>Tivat</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Netherlands

#### Amsterdam

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Anantara Grand Hotel Krasnapolsky Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Andaz Amsterdam Prinsengracht</td><td>Amsterdam</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>De L&#x27;Europe Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>INK Hotel Amsterdam – MGallery Collection</td><td>Amsterdam</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>InterContinental Amstel Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Kimpton DeWitt Amsterdam</td><td>Amsterdam</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Mandarin Oriental Conservatorium, Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Pillows Grand Boutique Hotel Maurits at the Park</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Pulitzer Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Rosewood Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Sofitel Legend The Grand Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>The Dylan Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>The Hoxton Lloyd Amsterdam</td><td>Amsterdam</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Tivoli Doelen</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>W Amsterdam</td><td>Amsterdam</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Waldorf Astoria Amsterdam</td><td>Amsterdam</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Maastricht

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Chateau Neercanne</td><td>Maastricht</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Rotterdam

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>nhow Rotterdam</td><td>Rotterdam</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### The Hague

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Hotel Des Indes</td><td>The Hague</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Valkenburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Netherlands"><td>Chateau St. Gerlach</td><td>Valkenburg</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Norway

#### Oslo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>Amerikalinjen</td><td>Oslo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>Hotel Continental</td><td>Oslo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>Sommerro</td><td>Oslo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>The Thief</td><td>Oslo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Skodje

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>Storfjord Hotel</td><td>Skodje</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Trondheim

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Norway"><td>Britannia Hotel</td><td>Trondheim</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Poland

#### Krakow

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Poland"><td>Hotel Saski Krakow, Curio Collection by Hilton</td><td>Krakow</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Warsaw

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Poland"><td>Hotel Bristol, a Luxury Collection Hotel, Warsaw</td><td>Warsaw</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Poland"><td>Nobu Hotel Warsaw</td><td>Warsaw</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Poland"><td>Raffles Europejski Warsaw</td><td>Warsaw</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Portugal

#### Albufeira

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Kimpton Atlantico Algarve</td><td>Albufeira</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Pine Cliffs Ocean Suites, a Luxury Collection Resort &amp; Spa, Algarve</td><td>Albufeira</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>W Algarve</td><td>Albufeira</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>W Residences Algarve</td><td>Albufeira</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Almancil

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Conrad Algarve</td><td>Almancil</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Carvoeiro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Tivoli Carvoeiro Algarve Resort</td><td>Carvoeiro</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Cascais

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Farol Hotel</td><td>Cascais</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Grande Real Villa Italia Hotel &amp; Spa</td><td>Cascais</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Legacy Hotel Cascais, Curio Collection by Hilton</td><td>Cascais</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Encarnação

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Aethos Ericeira</td><td>Encarnação</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Estoril

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>InterContinental Cascais-Estoril</td><td>Estoril</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Funchal

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Reid&#x27;s Palace, A Belmond Hotel, Madeira</td><td>Funchal</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Savoy Palace, Madeira Island</td><td>Funchal</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The Reserve, Madeira Island</td><td>Funchal</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Furnas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Furnas</td><td>Furnas</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lamego

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Six Senses Douro Valley</td><td>Lamego</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lisbon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Bairro Alto Hotel</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Convent Square Lisbon Hotel, Vignette Collection</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Corinthia Lisbon</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>DUO Hotel Lisbon, Curio Collection by Hilton</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Epic Sana Marques</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Four Seasons Hotel Ritz Lisbon</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Hyatt Regency Lisbon</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>InterContinental Lisbon</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>ME Lisbon</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>MYTHIC SANA Downtown Suites</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Olissippo Lapa Palace</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Palacio Ludovice Wine Experience Hotel</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Pousada de Lisboa - Praça do Comercio</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The Emerald House Lisbon, Curio Collection by Hilton</td><td>Lisbon</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The One Palacio da Anunciada</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Tivoli Avenida Liberdade Lisboa</td><td>Lisbon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Melides

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Vermelho</td><td>Melides</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Moncarapacho

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Vila Monte</td><td>Moncarapacho</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Monsaraz

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>São Lourenço do Barrocal</td><td>Monsaraz</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ponta Delgada

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Ponta Delgada</td><td>Ponta Delgada</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Porches

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Vila Vita Parc</td><td>Porches</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Portimão

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Bela Vista Hotel &amp; Spa - Adults Only</td><td>Portimão</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Porto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Cenica Porto Hotel, Curio Collection by Hilton</td><td>Porto</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Infante Sagres, Small Luxury Hotels of the World</td><td>Porto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>InterContinental Porto - Palacio das Cardosas</td><td>Porto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>NH Collection Porto Batalha</td><td>Porto</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The Largo</td><td>Porto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The One Monumental Palace</td><td>Porto</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Raiva Castelo de Paiva

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Octant Douro</td><td>Raiva Castelo de Paiva</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sintra

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Penha Longa Resort</td><td>Sintra</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tôr

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Viceroy at Ombria Algarve</td><td>Tôr</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vila Nova de Gaia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Boeira Garden Hotel Porto Gaia, Curio Collection by Hilton</td><td>Vila Nova de Gaia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Hilton Porto Gaia</td><td>Vila Nova de Gaia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The Yeatman</td><td>Vila Nova de Gaia</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>Tivoli Kopke Porto Gaia Hotel</td><td>Vila Nova de Gaia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vila do Conde

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Portugal"><td>The Lince Santa Clara Historic Hotel</td><td>Vila do Conde</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Romania

#### Bucharest

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Romania"><td>InterContinental Athenee Palace Bucharest</td><td>Bucharest</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Scotland

#### Alexandria

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>Cameron House on Loch Lomond</td><td>Alexandria</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Auchterarder

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>The Gleneagles Hotel</td><td>Auchterarder</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Edinburgh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>100 Princes Street</td><td>Edinburgh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>Gleneagles Townhouse</td><td>Edinburgh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>Kimpton Charlotte Square</td><td>Edinburgh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>The Balmoral, a Rocco Forte hotel</td><td>Edinburgh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>The Caledonian Edinburgh</td><td>Edinburgh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>W Edinburgh</td><td>Edinburgh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kelso

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>SCHLOSS Roxburghe</td><td>Kelso</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### St Andrews

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>Old Course Hotel, Golf Resort &amp; Spa</td><td>St Andrews</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>Rusacks St Andrews</td><td>St Andrews</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Turnberry

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Scotland"><td>Trump Turnberry, Scotland</td><td>Turnberry</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Serbia

#### Belgrade

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Serbia"><td>The St. Regis Hotel and Residences Belgrade</td><td>Belgrade</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Slovenia

#### Ljubljana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Slovenia"><td>InterContinental Ljubljana</td><td>Ljubljana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Spain

#### Alaior

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Torre Vella</td><td>Alaior</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Alicante

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Amerigo</td><td>Alicante</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>SHA Wellness Spain</td><td>Alicante</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Banyalbufar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Son Bunyola</td><td>Banyalbufar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Barcelona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Almanac Barcelona</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Claris Hotel &amp; Spa</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Cotton House Hotel Autograph Collection</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>El Palace Barcelona</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Grand Hotel Central</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Grand Hyatt Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hilton Diagonal Mar Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Arts Barcelona</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Neri Relais &amp; Chateaux</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>InterContinental Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Kimpton Vividora Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Le Meridien Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Barcelona</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Sitges Terramar</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Mandarin Oriental, Barcelona</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Monument Hotel</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>NH Collection Barcelona Gran Hotel Calderon</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Sofitel Barcelona Skipper</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Barcelona EDITION</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Hoxton, Poblenou</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The One Barcelona</td><td>Barcelona</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>W Barcelona</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Wittmore Hotel</td><td>Barcelona</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Bilbao

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Melia Bilbao</td><td>Bilbao</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>NH Collection Villa de Bilbao</td><td>Bilbao</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Artist Grand Hotel of Art</td><td>Bilbao</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Calvià

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Castell Son Claret</td><td>Calvià</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel de Mar, a Gran Melia Hotel</td><td>Calvià</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Mandarin Oriental Punta Negra, Mallorca</td><td>Calvià</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Canyamel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Cap Vermell Grand Hotel</td><td>Canyamel</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Capdepera

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Pleta De Mar Luxury By Nature</td><td>Capdepera</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cartagena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Grand Hyatt La Manga Club Golf and Spa</td><td>Cartagena</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Casares

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Finca Cortesín Hotel Golf &amp; Spa</td><td>Casares</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cordoba

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Palacio del Bailio</td><td>Cordoba</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Costa Adeje

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Bahia del Duque</td><td>Costa Adeje</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Deià

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>La Residencia, A Belmond Hotel, Mallorca</td><td>Deià</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Eivissa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Montesol Experimental Ibiza</td><td>Eivissa</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Standard, Ibiza</td><td>Eivissa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Elciego

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Marques de Riscal, a Luxury Collection Hotel, Elciego</td><td>Elciego</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Getxo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Palacio Arriluce Hotel</td><td>Getxo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Girona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Camiral Golf &amp; Wellness</td><td>Girona</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Granada

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Palacio de los Patos</td><td>Granada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Casa 1800 Granada</td><td>Granada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Melia Granada</td><td>Granada</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Seda Club Hotel</td><td>Granada</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Guia de Isora

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Ritz-Carlton, Abama</td><td>Guia de Isora</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ibiza

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel Ibiza Bay</td><td>Ibiza</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### La Caleta Costa Adeje Tenerife

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Royal Hideaway Corales Suites</td><td>La Caleta Costa Adeje Tenerife</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Las Palmas de Gran Canaria

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Paradisus by Melia Gran Canaria</td><td>Las Palmas de Gran Canaria</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Madrid

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>BRACH Madrid - Evok Collection</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Bless Hotel Madrid</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Casa de las Artes, a member of Melia Collection</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Four Seasons Hotel Madrid</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Gran Hotel Ingles</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Puerta de Alcala</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Fenix, a Gran Melia Hotel</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Montera Madrid, Curio Collection by Hilton</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Unico Madrid</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hyatt Centric Gran Via Madrid</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hyatt Regency Hesperia Madrid</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>InterContinental Madrid</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>JW Marriott Hotel Madrid</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Mandarin Oriental Ritz, Madrid</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>NH Collection Madrid Palacio de Tepa</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Palacio de los Duques, a Gran Melia Hotel</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Rosewood Villa Magna</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Santo Mauro, a Luxury Collection Hotel</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Madrid EDITION</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Palace, a Luxury Collection Hotel, Madrid</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Principal Madrid Hotel</td><td>Madrid</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Thompson Madrid</td><td>Madrid</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Marbella

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Anantara Villa Padierna Marbella</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Don Carlos Marbella</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>El Fuerte Marbella</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hacienda del Mar, The Melia Collection</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Kimpton Los Monteros Marbella</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>La Fonda Heritage Hotel</td><td>Marbella</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>La Zambra Resort</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Marbella</td><td>Marbella</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Marbella Club Hotel - Golf Resort &amp; Spa</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel Marbella</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Puente Romano Beach Resort</td><td>Marbella</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Menorca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Villa Le Blanc, a Gran Melia Hotel</td><td>Menorca</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montuiri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Finca Serena Mallorca</td><td>Montuiri</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Málaga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Gran Hotel Miramar GL</td><td>Málaga</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Ikos Andalusia</td><td>Málaga</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Malaga</td><td>Málaga</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Palma

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Can Bordoy Grand House GL Preferred Hotels &amp; Resorts</td><td>Palma</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Concepcio by Nobis</td><td>Palma</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Victoria, a Gran Melia Hotel</td><td>Palma</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobis Hotel Palma</td><td>Palma</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The St. Regis Mardavall Mallorca Resort</td><td>Palma</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Playa des Arenals

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Teranka Hotel Formentera</td><td>Playa des Arenals</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Port Soller

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Jumeirah Mallorca</td><td>Port Soller</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Port de Pollença

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Four Seasons Resort Mallorca at Formentor</td><td>Port de Pollença</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Port de Sant Miguel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Cala San Miguel Ibiza Resort, Curio Collection by Hilton</td><td>Port de Sant Miguel</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Porto Petro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Ikos Porto Petro</td><td>Porto Petro</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Puigpunyent

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Grand Hotel Son Net</td><td>Puigpunyent</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sa Pobla

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>The Lodge Mallorca</td><td>Sa Pobla</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Salamanca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hospes Palacio de San Esteban</td><td>Salamanca</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### San Sebastian

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Akelarre Relais &amp; Chateaux, San Sebastian</td><td>San Sebastian</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Maria Cristina, a Luxury Collection Hotel, San Sebastian</td><td>San Sebastian</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>NH Collection San Sebastian Aranzazu</td><td>San Sebastian</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Nobu Hotel San Sebastian</td><td>San Sebastian</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sant Antoni de Portmany

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>OKU Ibiza</td><td>Sant Antoni de Portmany</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sant Joan de Labritja

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Six Senses Ibiza</td><td>Sant Joan de Labritja</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sant Josep de Sa Talaia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Petunia Ibiza, a Beaumier Hotel</td><td>Sant Josep de Sa Talaia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sant Josep de sa Talaia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>7Pines Resort Ibiza</td><td>Sant Josep de sa Talaia</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Santa Eulalia del Rio

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Bless Ibiza Cala Nova</td><td>Santa Eulalia del Rio</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>ME Ibiza</td><td>Santa Eulalia del Rio</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Mondrian Ibiza</td><td>Santa Eulalia del Rio</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>W Ibiza</td><td>Santa Eulalia del Rio</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Santa Ponsa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Kimpton Aysla Mallorca</td><td>Santa Ponsa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Sardon de Duero

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Abadia Retuerta LeDomaine</td><td>Sardon de Duero</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Seville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Cavalta Boutique Hotel</td><td>Seville</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Alfonso XIII, a Luxury Collection Hotel, Seville</td><td>Seville</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Casa 1800 Sevilla</td><td>Seville</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Hotel Colon, a Gran Melia Hotel Seville</td><td>Seville</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sotogrande

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>SO/ Sotogrande Spa &amp; Golf Resort hotel</td><td>Sotogrande</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Teguise

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Paradisus by Melia Salinas Lanzarote</td><td>Teguise</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Torrent

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Mas de Torrent Hotel &amp; Spa</td><td>Torrent</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Valencia

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>Grand Hotel Centenari, Valencia, Autograph Collection</td><td>Valencia</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Spain"><td>NH Collection Valencia Colon</td><td>Valencia</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Sweden

#### Stockholm

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>At Six</td><td>Stockholm</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Grand Hotel Stockholm</td><td>Stockholm</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Hotel Diplomat</td><td>Stockholm</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Hotel Skeppsholmen</td><td>Stockholm</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Lydmar Hotel</td><td>Stockholm</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Nobis Hotel Stockholm</td><td>Stockholm</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Stockholm Stadshotell</td><td>Stockholm</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Sweden"><td>Villa Dagmar</td><td>Stockholm</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Switzerland

#### Andermatt

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Radisson Blu Hotel Reussen, Andermatt</td><td>Andermatt</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Chedi Andermatt</td><td>Andermatt</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ascona

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Castello del Sole Beach Resort &amp; SPA</td><td>Ascona</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bad Ragaz

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Grand Resort Bad Ragaz</td><td>Bad Ragaz</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Basel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Grand Hotel Les Trois Rois</td><td>Basel</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bern

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Bellevue Palace</td><td>Bern</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Schweizerhof Bern &amp; Spa</td><td>Bern</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Crans-Montana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Guarda Golf Hotel &amp; Residences</td><td>Crans-Montana</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Six Senses Crans-Montana</td><td>Crans-Montana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Davos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hard Rock Hotel Davos</td><td>Davos</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Engelberg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Kempinski Palace Engelberg</td><td>Engelberg</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Geneva

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Beau-Rivage, Geneva</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Four Seasons Hotel des Bergues Geneva</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel D&#x27;Angleterre Geneva</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Metropole Geneve</td><td>Geneva</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel President Wilson, a Luxury Collection Hotel, Geneva</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>InterContinental Geneve</td><td>Geneva</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>La Reserve Geneve Hotel and Spa</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Mandarin Oriental, Geneva</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Ritz-Carlton Hotel de la Paix, Geneva</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Woodward, Auberge Collection</td><td>Geneva</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Gonten

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Huus Quell By Appenzeller Huus</td><td>Gonten</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Gstaad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Gstaad Palace</td><td>Gstaad</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Alpina Gstaad</td><td>Gstaad</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Interlaken

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Victoria-Jungfrau Grand Hotel &amp; Spa</td><td>Interlaken</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lausanne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Beau-Rivage Palace Lausanne</td><td>Lausanne</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Angleterre</td><td>Lausanne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Lausanne Palace</td><td>Lausanne</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lucerne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Schweizerhof Luzern</td><td>Lucerne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Mandarin Oriental Palace, Luzern</td><td>Lucerne</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lugano

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Splendide Royal</td><td>Lugano</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Montreux

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Fairmont Le Montreux Palace</td><td>Montreux</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Obbuergen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Burgenstock Hotel and Alpine Spa</td><td>Obbuergen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Waldhotel by Buergenstock</td><td>Obbuergen</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Saas-Fee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Capra Saas-Fee</td><td>Saas-Fee</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### St. Moritz

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Carlton Hotel St. Moritz</td><td>St. Moritz</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Giardino Mountain</td><td>St. Moritz</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Grace La Margna St Moritz</td><td>St. Moritz</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Kulm Hotel St. Moritz</td><td>St. Moritz</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Suvretta House</td><td>St. Moritz</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Thalwil

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Alex Lake Zurich</td><td>Thalwil</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Vals

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>7132 Hotel</td><td>Vals</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Verbier

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>W Verbier</td><td>Verbier</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Vitznau

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Park Hotel Vitznau</td><td>Vitznau</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Zermatt

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Mont Cervin Palace</td><td>Zermatt</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Riffelalp Resort 2&#x27;222m</td><td>Zermatt</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Schweizerhof Zermatt</td><td>Zermatt</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Zurich

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Hotel Schweizerhof Zurich</td><td>Zurich</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>La Reserve Eden au Lac Zurich</td><td>Zurich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Mandarin Oriental Savoy, Zurich</td><td>Zurich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Park Hyatt Zurich</td><td>Zurich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Storchen Zurich</td><td>Zurich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>The Dolder Grand</td><td>Zurich</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Switzerland"><td>Widder Hotel</td><td>Zurich</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Turkey

#### Antalya

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Maxx Royal Kemer</td><td>Antalya</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bodrum

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Mandarin Oriental, Bodrum</td><td>Bodrum</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Susona Bodrum, LXR Hotels &amp; Resorts</td><td>Bodrum</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>The Bodrum EDITION</td><td>Bodrum</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Istanbul

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Aliee Istanbul - a Paris Society Collection Hotel</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Ciragan Palace Kempinski Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Four Seasons Hotel Istanbul at Sultanahmet</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Four Seasons Hotel Istanbul at the Bosphorus</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Mandarin Oriental Bosphorus, Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Park Hyatt Istanbul - Macka Palas</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Princes&#x27; Palace Resort</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Raffles Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Sanasaryan Han, A Luxury Collection Hotel, Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Shangri-La Bosphorus, Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>The Peninsula Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>The Ritz-Carlton, Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>The St. Regis Istanbul</td><td>Istanbul</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Marmaris

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>D Maris Bay</td><td>Marmaris</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mugla

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Maxx Royal Bodrum</td><td>Mugla</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nevsehir

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Museum Hotel</td><td>Nevsehir</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Uchisar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Turkey"><td>Argos in Cappadocia</td><td>Uchisar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Türkiye

#### Istanbul

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Altunizade Suites Istanbul, Curio Collection by Hilton</td><td>Istanbul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Hilton Istanbul Bosphorus</td><td>Istanbul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>JW Marriott Istanbul Bosphorus</td><td>Istanbul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Swissotel The Bosphorus</td><td>Istanbul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>The Bank Hotel Istanbul, a Member of Design Hotels</td><td>Istanbul</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Nevsehir

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="Türkiye"><td>Via Regia Cappadocia</td><td>Nevsehir</td><td>THC</td><td>—</td></tr>
</tbody></table>

### United Kingdom

#### Arundel

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Amberley Castle</td><td>Arundel</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Bath

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Homewood</td><td>Bath</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Broadway

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Lygon Arms Hotel</td><td>Broadway</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Cambridge

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Graduate by Hilton Cambridge</td><td>Cambridge</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Edinburgh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>InterContinental Edinburgh The George</td><td>Edinburgh</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Old Town Chambers, Autograph Collection</td><td>Edinburgh</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Hoxton Edinburgh</td><td>Edinburgh</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Virgin Hotels Edinburgh</td><td>Edinburgh</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Girvan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Glenapp Castle</td><td>Girvan</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Glasgow

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Kimpton Blythswood Square Hotel and Spa</td><td>Glasgow</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### London

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>100 Queen&#x27;s Gate Hotel London Kensington, Curio Collection by Hilton</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Aethos London Shoreditch</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>COMO Metropolitan London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Canopy by Hilton London City</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Conrad London St. James</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Guardsman Hotel &amp; Residences</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Hyatt Regency London - The Churchill</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Hyde London City</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>InterContinental London Park Lane</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>JW Marriott Grosvenor House London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Kimpton Fitzroy London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>London Hilton on Park Lane</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>London Marriott Hotel County Hall</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>London Marriott Hotel Park Lane</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>ME London Hotel</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Sea Containers London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Sofitel London St James</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>St Martins Lane London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Ampersand Hotel</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Athenaeum Hotel and Residences</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Bloomsbury</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The BoTree London, Curio Collection by Hilton</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Capital Hotel, Apartments &amp; Townhouse</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Dixon, Tower Bridge, Autograph Collection</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Hoxton Holborn</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Hoxton, Shoreditch</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Hoxton, Southwark</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Kensington Hotel</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Landmark London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Lowndes London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Mandrake Hotel</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Marylebone</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The May Fair Hotel London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Ned London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Newman</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Prince Akatoki London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Sheraton Grand London Park Lane</td><td>London</td><td>THC</td><td><a href="https://www.youtube.com/watch?v=GQtJvoOwsUo">Video</a></td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Soho Hotel</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Standard, London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Trafalgar St. James London, Curio Collection by Hilton</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Twenty Two London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Westin London City</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Treehouse London</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Vintry &amp; Mercer</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Virgin Hotels London Shoreditch</td><td>London</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>art&#x27;otel London Battersea Power Station</td><td>London</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Manchester

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Kimpton Clocktower Hotel</td><td>Manchester</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Edwardian Manchester</td><td>Manchester</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Treehouse Hotel Manchester</td><td>Manchester</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Narberth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Grove Narberth</td><td>Narberth</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Newbury

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Retreat Elcot Park</td><td>Newbury</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Oxford

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>The Randolph Hotel Oxford, a Graduate by Hilton</td><td>Oxford</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### St Andrews

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Europe" data-country="United Kingdom"><td>Fairmont St Andrews</td><td>St Andrews</td><td>THC</td><td>—</td></tr>
</tbody></table>

## Africa

### Egypt

#### Alexandria

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Hotel Alexandria at San Stefano</td><td>Alexandria</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cairo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Fairmont Nile City Cairo</td><td>Cairo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Hotel Cairo at The First Residence</td><td>Cairo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>The Nile Ritz-Carlton, Cairo</td><td>Cairo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>The St. Regis Cairo</td><td>Cairo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>The St. Regis New Capital, Cairo</td><td>Cairo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Waldorf Astoria Cairo Heliopolis</td><td>Cairo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Garden City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Hotel Cairo at Nile Plaza</td><td>Garden City</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Giza

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Giza Palace Hotel &amp; Spa</td><td>Giza</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sharm Ash Sheikh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Egypt"><td>Four Seasons Resort Sharm El Sheikh</td><td>Sharm Ash Sheikh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Israel

#### Hertsliya

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>The Ritz-Carlton, Herzliya</td><td>Hertsliya</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Jerusalem

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>King David Jerusalem</td><td>Jerusalem</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>Mamilla, Jerusalem</td><td>Jerusalem</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>The David Citadel, Jerusalem</td><td>Jerusalem</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>Waldorf Astoria Jerusalem</td><td>Jerusalem</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Shaharut

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>Six Senses Shaharut</td><td>Shaharut</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tel Aviv

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>InterContinental David Tel Aviv</td><td>Tel Aviv</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>The David Kempinski Tel Aviv</td><td>Tel Aviv</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>The Jaffa - Fattal Limited Edition</td><td>Tel Aviv</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>The Setai Tel Aviv Hotel</td><td>Tel Aviv</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Israel"><td>The Vista at Hilton Tel Aviv</td><td>Tel Aviv</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Jordan

#### Amman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Jordan"><td>Four Seasons Hotel Amman</td><td>Amman</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Jordan"><td>The St. Regis Amman</td><td>Amman</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Kenya

#### Masai Mara

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Kenya"><td>JW Marriott Masai Mara Lodge</td><td>Masai Mara</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nairobi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Kenya"><td>Hemingways Nairobi</td><td>Nairobi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Kenya"><td>Kwetu Nairobi, Curio Collection by Hilton</td><td>Nairobi</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Kuwait

#### Kuwait City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Kuwait"><td>Four Seasons Hotel Kuwait at Burj Alshaya</td><td>Kuwait City</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Kuwait"><td>The St. Regis Kuwait</td><td>Kuwait City</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Kuwait"><td>Waldorf Astoria Kuwait</td><td>Kuwait City</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Mauritius

#### Beauchamp

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>Four Seasons Resort Mauritius at Anahita</td><td>Beauchamp</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Flacq

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>One&amp;Only Le Saint Geran</td><td>Flacq</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Flic en Flac

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>Maradiva Villas Resort &amp; Spa</td><td>Flic en Flac</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Le Morne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>The St. Regis Le Morne Resort, Mauritius</td><td>Le Morne</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Quatre Cocos

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>LUX Belle Mare</td><td>Quatre Cocos</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Trou d'Eau Douce

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mauritius"><td>Shangri-La Le Touessrok, Mauritius</td><td>Trou d&#x27;Eau Douce</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Morocco

#### Asni

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Kasbah Tamadot</td><td>Asni</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Casablanca

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Four Seasons Hotel Casablanca</td><td>Casablanca</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Royal Mansour Casablanca</td><td>Casablanca</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Fnideq

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>The St. Regis La Bahia Blanca Resort, Tamuda Bay</td><td>Fnideq</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Marrakech

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Amanjena</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Four Seasons Resort Marrakech</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>La Mamounia</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Mandarin Oriental, Marrakech</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Nobu Hotel Marrakech</td><td>Marrakech</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Park Hyatt Marrakech</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Royal Mansour Marrakech</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Selman Marrakech</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>The Oberoi, Marrakech</td><td>Marrakech</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Rabat

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Conrad Rabat Arzana</td><td>Rabat</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Waldorf Astoria Rabat Sale</td><td>Rabat</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tangier

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Morocco"><td>Fairmont Tazi Palace Tangier</td><td>Tangier</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Mozambique

#### Vilankulo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Mozambique"><td>Kisawa Sanctuary</td><td>Vilankulo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Oman

#### Al Jabal Al Akhdar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Oman"><td>Alila Jabal Akhdar</td><td>Al Jabal Al Akhdar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dibba

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Oman"><td>Six Senses Zighy Bay</td><td>Dibba</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Muscat

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Oman"><td>Mandarin Oriental, Muscat</td><td>Muscat</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Oman"><td>The Chedi Muscat</td><td>Muscat</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Oman"><td>The St. Regis Al Mouj Muscat Resort</td><td>Muscat</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Qatar

#### Doha

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Four Seasons Hotel Doha</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Katara Hills Doha, LXR Hotels &amp; Resorts</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Mandarin Oriental, Doha</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Maysan Doha, LXR Hotels &amp; Resorts</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Raffles Doha</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Rosewood Doha</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Sharq Village &amp; Spa</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>The Plaza Doha, LXR Hotels &amp; Resorts</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>The Ritz-Carlton, Doha</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>The St. Regis Doha</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>The St. Regis Marsa Arabia Island, The Pearl - Qatar</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Waldorf Astoria Doha Lusail</td><td>Doha</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Qatar"><td>Waldorf Astoria Doha West Bay</td><td>Doha</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Rwanda

#### Gisakura

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Rwanda"><td>One&amp;Only Nyungwe House</td><td>Gisakura</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kinigi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Rwanda"><td>One&amp;Only Gorilla&#x27;s Nest</td><td>Kinigi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Saudi Arabia

#### AlUla

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>Banyan Tree AlUla</td><td>AlUla</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Jeddah

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>Rosewood Jeddah</td><td>Jeddah</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Riyadh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>Four Seasons Hotel Riyadh at Kingdom Centre</td><td>Riyadh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>Mandarin Oriental Al Faisaliah, Riyadh</td><td>Riyadh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>The St. Regis Riyadh</td><td>Riyadh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tabuk

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>Nujuma, a Ritz-Carlton Reserve</td><td>Tabuk</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>The Red Sea EDITION</td><td>Tabuk</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Umluj

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>Six Senses Southern Dunes, The Red Sea</td><td>Umluj</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ummahat Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Saudi Arabia"><td>The St. Regis Red Sea</td><td>Ummahat Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Seychelles

#### Desroches Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Four Seasons Resort Seychelles at Desroches Island</td><td>Desroches Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mahe

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Canopy by Hilton Seychelles Resort</td><td>Mahe</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Cheval Blanc Seychelles</td><td>Mahe</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mahe Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Four Seasons Resort Seychelles</td><td>Mahe Island</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Mango House Seychelles, LXR Hotels &amp; Resorts</td><td>Mahe Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Platte Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Waldorf Astoria Seychelles Platte Island</td><td>Platte Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Praslin Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Seychelles"><td>Raffles Seychelles</td><td>Praslin Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### South Africa

#### Cape Town

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>12 Apostles Hotel and Spa</td><td>Cape Town</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Canopy by Hilton Cape Town Longkloof</td><td>Cape Town</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Cape Grace, A Fairmont Managed Hotel</td><td>Cape Town</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>InterContinental Table Bay Cape Town</td><td>Cape Town</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Mount Nelson, A Belmond Hotel, Cape Town</td><td>Cape Town</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>One&amp;Only Cape Town</td><td>Cape Town</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>The Cellars-Hohenort Hotel &amp; Spa</td><td>Cape Town</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Franschhoek

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Le Quartier Francais</td><td>Franschhoek</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hoedspruit

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Jabulani Safari</td><td>Hoedspruit</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Johannesburg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Four Seasons Hotel The Westcliff</td><td>Johannesburg</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Park Hyatt Johannesburg</td><td>Johannesburg</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Saxon Hotel, Villas and Spa</td><td>Johannesburg</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ladysmith

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Esiweni Safari Lodge</td><td>Ladysmith</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Plettenberg Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>The Plettenberg Hotel &amp; Spa</td><td>Plettenberg Bay</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Somerset West

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>Erinvale Estate Hotel &amp; Spa</td><td>Somerset West</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Umhlanga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="South Africa"><td>The Oyster Box</td><td>Umhlanga</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Tanzania

#### Arusha

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tanzania"><td>Ngorongoro Lodge</td><td>Arusha</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mafia Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tanzania"><td>Thanda Island</td><td>Mafia Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Robanda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tanzania"><td>Mapito Safari Camp, Serengeti, Autograph Collection</td><td>Robanda</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Serengeti National Park

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tanzania"><td>Four Seasons Safari Lodge Serengeti</td><td>Serengeti National Park</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="Tanzania"><td>Melia Serengeti Lodge</td><td>Serengeti National Park</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Zanzibar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tanzania"><td>Park Hyatt Zanzibar</td><td>Zanzibar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Tunisia

#### La Marsa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Tunisia"><td>Four Seasons Hotel Tunis</td><td>La Marsa</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### United Arab Emirates

#### Abu Dhabi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Al Wathba, a Luxury Collection Desert Resort &amp; Spa, Abu Dhabi</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Anantara Qasr Al Sarab Desert Resort</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Conrad Abu Dhabi Etihad Towers</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Emirates Palace Mandarin Oriental, Abu Dhabi</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Four Seasons Hotel Abu Dhabi at Maryah Island</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Rosewood Abu Dhabi</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Ritz-Carlton Abu Dhabi, Grand Canal</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The St. Regis Abu Dhabi</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The St. Regis Saadiyat Island Resort, Abu Dhabi</td><td>Abu Dhabi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ajman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Ajman Saray, a Luxury Collection Resort, Ajman</td><td>Ajman</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dubai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Al Habtoor Palace</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Al Maha, a Luxury Collection Desert Resort &amp; Spa, Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Armani Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Bab Al Shams</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Banyan Tree Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Bvlgari Resort Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Four Seasons Dubai at Jumeirah Beach</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Four Seasons Hotel Dubai International Financial Centre</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Jumeirah Al Naseem</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Jumeirah Al Qasr</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Jumeirah Dar Al Masyaf</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Jumeirah Marsa Al Arab</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Jumeirah Zabeel Saray</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Mandarin Oriental Downtown, Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Mandarin Oriental Jumeira, Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>One&amp;Only One Za&#x27;abeel</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>One&amp;Only The Palm</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Park Hyatt Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Raffles Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Raffles The Palm Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Biltmore Hotel Villas</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Lana - Dorchester Collection</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Ritz-Carlton, Dubai International Financial Centre</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Ritz-Carlton, Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Royal Atlantis Resort &amp; Residences FZE</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The St. Regis Downtown Dubai</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The St. Regis Dubai, The Palm</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Waldorf Astoria Dubai International Financial Centre</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Waldorf Astoria Dubai Palm Jumeirah</td><td>Dubai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Fujairah

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>InterContinental Fujairah Resort</td><td>Fujairah</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ras Al Khaimah

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Ritz-Carlton Ras Al Khaimah, Al Hamra Beach</td><td>Ras Al Khaimah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>The Ritz-Carlton Ras Al Khaimah, Al Wadi Desert</td><td>Ras Al Khaimah</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Africa" data-country="United Arab Emirates"><td>Waldorf Astoria Ras Al Khaimah</td><td>Ras Al Khaimah</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Zambia

#### Livingstone

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Africa" data-country="Zambia"><td>The Royal Livingstone Victoria Falls Zambia Hotel by Anantara</td><td>Livingstone</td><td>FHR</td><td>—</td></tr>
</tbody></table>

## Middle East

### Bahrain

#### Manama

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Bahrain"><td>Conrad Bahrain Financial Harbour</td><td>Manama</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Bahrain"><td>Four Seasons Hotel Bahrain Bay</td><td>Manama</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Bahrain"><td>The Ritz-Carlton, Bahrain</td><td>Manama</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Israel

#### Tel Aviv

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>Elkonin Tel Aviv Hotel - MGallery Collection</td><td>Tel Aviv</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>Hilton Tel Aviv</td><td>Tel Aviv</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="Israel"><td>The Drisco</td><td>Tel Aviv</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Qatar

#### Doha

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="Qatar"><td>Mondrian Doha</td><td>Doha</td><td>THC</td><td>—</td></tr>
</tbody></table>

### United Arab Emirates

#### Abu Dhabi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Fairmont Bab Al Bahr, Abu Dhabi</td><td>Abu Dhabi</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Sofitel Abu Dhabi Corniche</td><td>Abu Dhabi</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>The Abu Dhabi EDITION</td><td>Abu Dhabi</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>The WB Abu Dhabi, Curio Collection By Hilton</td><td>Abu Dhabi</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Dubai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Atlantis The Palm</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Canopy by Hilton Dubai Al Seef</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Conrad Dubai</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Jumeirah Beach Hotel</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Jumeirah Mina Al Salam</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Rixos Premium Dubai</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>SIRO One Za&#x27;abeel</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>SLS Dubai Hotel and Residences</td><td>Dubai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Middle East" data-country="United Arab Emirates"><td>Taj Dubai</td><td>Dubai</td><td>THC</td><td>—</td></tr>
</tbody></table>

## Asia

### Cambodia

#### Phnom Penh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Sofitel Phnom Penh Phokeethra</td><td>Phnom Penh</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Raffles Hotel Le Royal</td><td>Phnom Penh</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Rosewood Phnom Penh</td><td>Phnom Penh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Siem Reap

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Sofitel Angkor Phokeethra Golf &amp; Spa Resort</td><td>Siem Reap</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Amansara</td><td>Siem Reap</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Park Hyatt Siem Reap</td><td>Siem Reap</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Raffles Grand Hotel d&#x27;Angkor</td><td>Siem Reap</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### China

#### Beijing

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Beijing</td><td>Beijing</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Fairmont Beijing</td><td>Beijing</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Grand Hyatt Beijing</td><td>Beijing</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Bvlgari Hotel Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>China World Summit Wing, Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental Qianmen, Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental Wangfujing, Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Park Hyatt Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Rosewood Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Peninsula Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The PuXuan Hotel and SPA</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Waldorf Astoria Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Xitan Hotel Beijing</td><td>Beijing</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Guangzhou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Guangzhou</td><td>Guangzhou</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Guangzhou, China</td><td>Guangzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental, Guangzhou</td><td>Guangzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Rosewood Guangzhou</td><td>Guangzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Guangzhou</td><td>Guangzhou</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hangzhou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Hangzhou</td><td>Hangzhou</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Amanfayun</td><td>Hangzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Hangzhou at West Lake</td><td>Hangzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Midtown Shangri-La, Hangzhou</td><td>Hangzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Silk Lakehouse, Shangri-La Hangzhou</td><td>Hangzhou</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lhasa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Shangri-La Lhasa</td><td>Lhasa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Shanghai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Grand Hyatt Shanghai</td><td>Shanghai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>W Shanghai The Bund</td><td>Shanghai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Alila Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Amanyangyun</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Bvlgari Hotel Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Capella Shanghai Jian Ye Li</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>J Hotel Shanghai Tower</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Jing An Shangri-La, Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental Pudong, Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Park Hyatt Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Pudong Shangri-La, Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Regent Shanghai Pudong</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Langham, Shanghai, Xintiandi</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Peninsula Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The PuLi Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton Shanghai, Pudong</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Shanghai EDITION</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Shanghai Jingan</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis on the Bund, Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Upper House Shanghai</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Waldorf Astoria Shanghai Qiantan</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Waldorf Astoria Shanghai on the Bund</td><td>Shanghai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Wuzhen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Alila Wuzhen</td><td>Wuzhen</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Hong Kong

#### Hong Kong

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>Cordis, Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>JW Marriott Hotel Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>Kerry Hotel, Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>Kimpton Tsim Sha Tsui Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>Lanson Place Causeway Bay, Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>Mondrian Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>The Hari Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Hong Kong"><td>W Hong Kong</td><td>Hong Kong</td><td>THC</td><td>—</td></tr>
</tbody></table>

### India

#### Bambolim

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Grand Hyatt Goa</td><td>Bambolim</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Bengaluru

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>JW Marriott Bengaluru Prestige Golfshire Resort and Spa</td><td>Bengaluru</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Four Seasons Hotel Bengaluru at Embassy ONE</td><td>Bengaluru</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Leela Palace Bengaluru</td><td>Bengaluru</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Ritz-Carlton, Bangalore</td><td>Bengaluru</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Coorg

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Madikeri Resort &amp; Spa, Coorg</td><td>Coorg</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Kochi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Malabar Resort &amp; Spa</td><td>Kochi</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Majorda

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Alila Diwa Goa</td><td>Majorda</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Mumbai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Sofitel Mumbai BKC</td><td>Mumbai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Four Seasons Mumbai</td><td>Mumbai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi, Mumbai</td><td>Mumbai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Taj Mahal Palace, Mumbai</td><td>Mumbai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Narendra Nagar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Westin Resort and Spa Himalayas</td><td>Narendra Nagar</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### New Delhi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Shangri-La Eros, New Delhi</td><td>New Delhi</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Mahal New Delhi</td><td>New Delhi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Imperial New Delhi</td><td>New Delhi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Leela Palace New Delhi</td><td>New Delhi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Lodhi New Delhi</td><td>New Delhi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi, New Delhi</td><td>New Delhi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Indonesia

#### Badung

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Desa Potato Head Bali</td><td>Badung</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Laguna, a Luxury Collection Resort &amp; Spa, Bali</td><td>Badung</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Aman Villas at Nusa Dua</td><td>Badung</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Jimbaran Puri, A Belmond Hotel, Bali</td><td>Badung</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Raffles Bali</td><td>Badung</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Umana Bali, LXR Hotels &amp; Resorts</td><td>Badung</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bali

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Cicada Resort Bali Ubud, Autograph Collection</td><td>Bali</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Apurva Kempinski Bali</td><td>Bali</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Jakarta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Fairmont Jakarta</td><td>Jakarta</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Grand Hyatt Jakarta</td><td>Jakarta</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Four Seasons Hotel Jakarta</td><td>Jakarta</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Mandarin Oriental, Jakarta</td><td>Jakarta</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Langham, Jakarta</td><td>Jakarta</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The St. Regis Jakarta</td><td>Jakarta</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Seminyak

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Hotel Indigo Bali Seminyak Beach</td><td>Seminyak</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>W Bali Seminyak</td><td>Seminyak</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Alila Seminyak</td><td>Seminyak</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Legian Seminyak, Bali</td><td>Seminyak</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tanjung Benoa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Conrad Bali</td><td>Tanjung Benoa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Ubud

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>COMO Uma Ubud</td><td>Ubud</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Gdas Bali Health &amp; Wellness Resort</td><td>Ubud</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Viceroy Bali</td><td>Ubud</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Amandari</td><td>Ubud</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>COMO Shambhala Estate</td><td>Ubud</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Capella Ubud, Bali</td><td>Ubud</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Four Seasons Resort Bali at Sayan</td><td>Ubud</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Mandapa, a Ritz-Carlton Reserve</td><td>Ubud</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Japan

#### Hakone

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hotel Indigo Hakone Gora</td><td>Hakone</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hyatt Regency Hakone Resort and Spa</td><td>Hakone</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>ESPACIO The Hakone Geihinkan Rin Poh Ki Ryu</td><td>Hakone</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ishigaki

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>ANA InterContinental Ishigaki Resort</td><td>Ishigaki</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Kanazawa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hyatt Centric Kanazawa</td><td>Kanazawa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Karuizawa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hotel Indigo Karuizawa</td><td>Karuizawa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Kyoto

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Ace Hotel Kyoto</td><td>Kyoto</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hilton Kyoto</td><td>Kyoto</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hyatt Regency Kyoto</td><td>Kyoto</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Westin Miyako Kyoto</td><td>Kyoto</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Aman Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Banyan Tree Higashiyama Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Dusit Thani Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>FAUCHON L&#x27;Hotel Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>HOTEL THE MITSUI KYOTO, a Luxury Collection Hotel &amp; Spa</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Imperial Hotel, Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Park Hyatt Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>ROKU KYOTO, LXR Hotels &amp; Resorts</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Six Senses Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Suiran, a Luxury Collection Hotel, Kyoto</td><td>Kyoto</td><td>FHR</td><td><a href="https://visitkarma.com/p/suiran-kyoto-arashiyama-review-marriott-luxury-collection-onsen-ryokan-stay/">Blog</a> · <a href="https://www.youtube.com/watch?v=RJSN7wgPO40">Video</a></td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Hotel Seiryu Kyoto Kiyomizu</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Kyoto</td><td>Kyoto</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Miyakojima

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hilton Okinawa Miyako Island Resort</td><td>Miyakojima</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>IRAPH SUI, a Luxury Collection Hotel, Miyako Okinawa</td><td>Miyakojima</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Rosewood Miyakojima</td><td>Miyakojima</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nagasaki

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Nagasaki Marriott Hotel</td><td>Nagasaki</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Okinawa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hilton Okinawa Sesoko Resort</td><td>Okinawa</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hyatt Regency Seragaki Island, Okinawa</td><td>Okinawa</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Halekulani Okinawa</td><td>Okinawa</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Osaka

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Canopy by Hilton Osaka Umeda</td><td>Osaka</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Osaka Station Hotel, Autograph Collection</td><td>Osaka</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Conrad Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>InterContinental Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Patina Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The St. Regis Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>W Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Waldorf Astoria Osaka</td><td>Osaka</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sapporo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hotel Sosei Sapporo – MGallery Collection</td><td>Sapporo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>InterContinental Sapporo</td><td>Sapporo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tokyo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>ANA InterContinental Tokyo</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hilton Tokyo</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>JW Marriott Hotel Tokyo</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Kimpton Shinjuku Tokyo</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Capitol Hotel Tokyu</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Prince Park Tower Tokyo</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Prince Sakura Tower Tokyo, Autograph Collection</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Tokyo Station Hotel</td><td>Tokyo</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>1 Hotel Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Aman Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Andaz Tokyo Toranomon Hills</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>BELLUSTAR TOKYO, A Pan Pacific Hotel</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Bvlgari Hotel Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Conrad Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Fairmont Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Tokyo at Marunouchi</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Four Seasons Hotel Tokyo at Otemachi</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Grand Hyatt Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Hotel New Otani Tokyo Executive House Zen</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Janu Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Mandarin Oriental, Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Palace Hotel Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Park Hyatt Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Shangri-La Tokyo</td><td>Tokyo</td><td>FHR</td><td><a href="https://www.youtube.com/watch?v=0-9yoNhmLtk">Video</a></td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Okura Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Peninsula Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Prince Gallery Tokyo Kioicho, a Luxury Collection Hotel</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Tokyo</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Tokyo EDITION, Ginza</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Tokyo EDITION, Toranomon</td><td>Tokyo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Yokohama

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Westin Yokohama, Greater Tokyo</td><td>Yokohama</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Kahala Hotel &amp; Resort Yokohama</td><td>Yokohama</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Maldives

#### Raa Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>The Standard, Huruvalhi Maldives</td><td>Raa Atoll</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>JOALI Being</td><td>Raa Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>JOALI Maldives</td><td>Raa Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Philippines

#### Makati City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Fairmont Makati Manila</td><td>Makati City</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Raffles Makati</td><td>Makati City</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>The Peninsula Manila</td><td>Makati City</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pasay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Conrad Manila</td><td>Pasay</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Singapore

#### Singapore

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Andaz Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>COMO Metropolitan Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Conrad Singapore Orchard</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Fairmont Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Grand Hyatt Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Mondrian Singapore Duxton</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>PARKROYAL COLLECTION Pickering, Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Pan Pacific Orchard, Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Pan Pacific Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>QT Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Shangri-La Rasa Sentosa, Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Barracks Hotel Sentosa</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Standard, Singapore</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>W Singapore Sentosa Cove</td><td>Singapore</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Artyzen Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Capella Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Conrad Singapore Marina Bay</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Four Seasons Hotel Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Mandai Rainforest Resort by Banyan Tree</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Mandarin Oriental, Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Marina Bay Sands</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Raffles Hotel, Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>Shangri-La Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Capitol Kempinski Hotel Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Fullerton Bay Hotel Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Laurus, a Luxury Collection Resort, Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Ritz-Carlton, Millenia Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The Singapore EDITION</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Singapore"><td>The St. Regis Singapore</td><td>Singapore</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### South Korea

#### Seoul

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Andaz Seoul Gangnam</td><td>Seoul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>JW Marriott Hotel Seoul</td><td>Seoul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Lotte Hotel Seoul</td><td>Seoul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Mondrian Seoul Itaewon</td><td>Seoul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>The Westin Seoul Parnas</td><td>Seoul</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Conrad Seoul</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Fairmont Ambassador Seoul</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Four Seasons Hotel Seoul</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Grand Hyatt Seoul</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Grand InterContinental Seoul Parnas</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Park Hyatt Seoul</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>SIGNIEL SEOUL</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>The Shilla Seoul</td><td>Seoul</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Sri Lanka

#### Habaraduwa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Sri Lanka"><td>The Fortress Resort &amp; Spa</td><td>Habaraduwa</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Thailand

#### Bangkok

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>137 Pillars Suites Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>COMO Metropolitan Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Conrad Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Grand Hyatt Erawan Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>JW Marriott Hotel Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>KROMO Bangkok, Curio Collection by Hilton</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Madi Paidi Bangkok, Autograph Collection</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>SO/ Bangkok</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Sofitel Bangkok Sukhumvit</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Standard, Bangkok Mahanakhon</td><td>Bangkok</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Aman Nai Lert Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Siam Bangkok Hotel</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Capella Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Dusit Thani Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Hotel Bangkok at Chao Phraya River</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Kimpton Maa-Lai Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Mandarin Oriental, Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Park Hyatt Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Rosewood Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Siam Kempinski Hotel Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Sindhorn Kempinski Hotel Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Peninsula Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Ritz-Carlton, Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Siam</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The St. Regis Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Waldorf Astoria Bangkok</td><td>Bangkok</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Chiang Mai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>AMANOR Hotel Chiang Mai</td><td>Chiang Mai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Aleenta Retreat Chiang Mai</td><td>Chiang Mai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Chiang Mai The Mae Ping</td><td>Chiang Mai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Melia Chiang Mai</td><td>Chiang Mai</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>137 Pillars House Chiang Mai</td><td>Chiang Mai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Chiang Mai Resort</td><td>Chiang Mai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Resort Chiang Mai</td><td>Chiang Mai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Raya Heritage Chiang Mai</td><td>Chiang Mai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Chon Buri

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Standard, Pattaya Na Jomtien</td><td>Chon Buri</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Andaz Pattaya Jomtien Beach</td><td>Chon Buri</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Mason</td><td>Chon Buri</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Koh Samui

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Hyatt Regency Koh Samui</td><td>Koh Samui</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Melia Koh Samui</td><td>Koh Samui</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>W Koh Samui</td><td>Koh Samui</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Banyan Tree Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Conrad Koh Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Resort Koh Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Kimpton Kitalay Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Six Senses Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Ritz-Carlton Koh Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Vana Belle, A Luxury Collection Resort, Koh Samui</td><td>Koh Samui</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Petchaburi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>SO/ Hua Hin</td><td>Petchaburi</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Phuket

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Dinso Resort and Villas Phuket, Vignette Collection</td><td>Phuket</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Phuket Resort</td><td>Phuket</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>JW Marriott Phuket, Resort &amp; Spa</td><td>Phuket</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Melia Phuket Mai Khao</td><td>Phuket</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>SAii Laguna Phuket</td><td>Phuket</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Twinpalms Phuket</td><td>Phuket</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Amanpuri</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Layan Phuket Resort</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Banyan Tree Phuket</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Keemala</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Rosewood Phuket</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Naka Island, a Luxury Collection Resort &amp; Spa, Phuket</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Trisara</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>V Villas Phuket Mgallery Collection</td><td>Phuket</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Prachuap Khiri Khan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Hua Hin Resort</td><td>Prachuap Khiri Khan</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>The Standard, Hua Hin</td><td>Prachuap Khiri Khan</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Takuapa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>JW Marriott Khao Lak Resort &amp; Spa</td><td>Takuapa</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Vietnam

#### Danang

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Hyatt Regency Danang Resort and Spa</td><td>Danang</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>InterContinental Danang Sun Peninsula Resort</td><td>Danang</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hanoi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Melia Hanoi Hotel</td><td>Hanoi</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Pan Pacific Hanoi</td><td>Hanoi</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Capella Hanoi</td><td>Hanoi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Fairmont Hanoi</td><td>Hanoi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Sofitel Legend Metropole Hanoi</td><td>Hanoi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ho Chi Minh City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Hotel des Arts Saigon – MGallery Hotel Collection</td><td>Ho Chi Minh City</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Park Hyatt Saigon</td><td>Ho Chi Minh City</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>The Reverie Saigon</td><td>Ho Chi Minh City</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hoi An

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Moire Hoi An, Vignette Collection</td><td>Hoi An</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Khanh Hoa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>JW Marriott Cam Ranh Bay Resort &amp; Spa</td><td>Khanh Hoa</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Phu Quoc

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>La Festa Phu Quoc, Curio Collection by Hilton</td><td>Phu Quoc</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>New World Phu Quoc Resort</td><td>Phu Quoc</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>JW Marriott PhuQuoc Emerald Bay Resort &amp; Spa</td><td>Phu Quoc</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Regent Phu Quoc</td><td>Phu Quoc</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Bhutan

#### Paro

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Bhutan"><td>Amankora</td><td>Paro</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Thimphu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Bhutan"><td>Six Senses Bhutan</td><td>Thimphu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Cambodia

#### Sihanoukville

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Cambodia"><td>Six Senses Krabey Island</td><td>Sihanoukville</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### China

#### Chengdu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Six Senses Qing Cheng Mountain</td><td>Chengdu</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Chengdu</td><td>Chengdu</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Upper House Chengdu</td><td>Chengdu</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Waldorf Astoria Chengdu</td><td>Chengdu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Chongqing

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Chongqing</td><td>Chongqing</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hainan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Capella Tufu Bay, Hainan</td><td>Hainan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hong Kong

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Grand Hyatt Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Island Shangri-La, Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental The Landmark, Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental, Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Regent Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Rosewood Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Murray, Hong Kong, a Niccolo Hotel</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Peninsula Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Upper House Hong Kong</td><td>Hong Kong</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lijiang

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Amandayan</td><td>Lijiang</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Macau

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Macao</td><td>Macau</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental, Macau</td><td>Macau</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Macao</td><td>Macau</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nanjing

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Nanjing</td><td>Nanjing</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Qingdao

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Qingdao</td><td>Qingdao</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sanya

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental, Sanya</td><td>Sanya</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Rosewood Sanya</td><td>Sanya</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Sanya Yalong Bay Resort</td><td>Sanya</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Shenzhen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Conrad Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Mandarin Oriental, Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Park Hyatt Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Raffles Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Shangri-La Nanshan, Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Shenzhen Bao&#x27;an</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Shenzhen</td><td>Shenzhen</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sichuan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Rissai Valley, a Ritz-Carlton Reserve</td><td>Sichuan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Suzhou

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Suzhou</td><td>Suzhou</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton Suzhou</td><td>Suzhou</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tianjin

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Four Seasons Hotel Tianjin</td><td>Tianjin</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Tianjin</td><td>Tianjin</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Xiamen

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Lohkah Hotel &amp; Spa</td><td>Xiamen</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Waldorf Astoria Xiamen</td><td>Xiamen</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Xian

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>Sofitel Legend People&#x27;s Grand Hotel Xian</td><td>Xian</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The Ritz-Carlton, Xian</td><td>Xian</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Zhuhai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="China"><td>The St. Regis Zhuhai</td><td>Zhuhai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### India

#### Agra

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi Amarvilas, Agra</td><td>Agra</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ajabgarh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Amanbagh</td><td>Ajabgarh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bardez

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>W Goa</td><td>Bardez</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Benaulim

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Exotica Resort &amp; Spa, Goa</td><td>Benaulim</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Cavelossim

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>St. Regis Goa Resort</td><td>Cavelossim</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Chennai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Leela Palace Chennai</td><td>Chennai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dehradun

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Six Senses Vana - A Wellness Retreat</td><td>Dehradun</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Gurgaon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi, Gurgaon</td><td>Gurgaon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hyderabad

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Falaknuma Palace</td><td>Hyderabad</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Jaipur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Alila Fort Bishangarh</td><td>Jaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Raffles Jaipur</td><td>Jaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Rambagh Palace</td><td>Jaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Leela Palace Jaipur</td><td>Jaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi Rajvilas</td><td>Jaipur</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Jodhpur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Umaid Bhawan Palace</td><td>Jodhpur</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mohali

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi Sukhvilas Resort &amp; Spa</td><td>Mohali</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Rishikesh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Rishikesh Resort &amp; Spa, Uttarakhand</td><td>Rishikesh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sawai Madhopur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Aman-i-Khas</td><td>Sawai Madhopur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Six Senses Fort Barwara</td><td>Sawai Madhopur</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Shimla

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Wildflower Hall</td><td>Shimla</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Udaipur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Raffles Udaipur</td><td>Udaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>Taj Lake Palace, Udaipur</td><td>Udaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Leela Palace Udaipur</td><td>Udaipur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="India"><td>The Oberoi Udaivilas, Udaipur</td><td>Udaipur</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Indonesia

#### Bintan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Sanchaya</td><td>Bintan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Canggu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Regent Bali Canggu</td><td>Canggu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Denpasar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Andaz Bali</td><td>Denpasar</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Four Seasons Resort Bali at Jimbaran Bay</td><td>Denpasar</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The Ritz-Carlton, Bali</td><td>Denpasar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Labuan Bajo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>TAAKTANA, a Luxury Collection Resort &amp; Spa, Labuan Bajo</td><td>Labuan Bajo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Magelang

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Amanjiwo</td><td>Magelang</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Manggis

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Amankila</td><td>Manggis</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Moyo Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Amanwana</td><td>Moyo Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nusa Dua

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>The St. Regis Bali Resort</td><td>Nusa Dua</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Payangan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Buahan, a Banyan Tree Escape</td><td>Payangan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pecatu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Alila Villas Uluwatu</td><td>Pecatu</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Jumeirah Bali</td><td>Pecatu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sumba

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>NIHI Sumba</td><td>Sumba</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tabanan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Soori Bali</td><td>Tabanan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Uluwatu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Indonesia"><td>Bvlgari Resort Bali</td><td>Uluwatu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Japan

#### Beppu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>ANA InterContinental Beppu Resort &amp; Spa</td><td>Beppu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Fukuoka

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton Fukuoka</td><td>Fukuoka</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nago

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Okinawa</td><td>Nago</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nagoya

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>ESPACIO Nagoya Castle</td><td>Nagoya</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>TIAD, Autograph Collection</td><td>Nagoya</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nara

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>JW Marriott Hotel Nara</td><td>Nara</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nikko

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Ritz-Carlton, Nikko</td><td>Nikko</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Niseko

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Park Hyatt Niseko Hanazono</td><td>Niseko</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>The Higashiyama Niseko Village, a Ritz Carlton Reserve</td><td>Niseko</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Onomichi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Azumi Setoda</td><td>Onomichi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Shima-shi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Amanemu</td><td>Shima-shi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Shizuoka

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Japan"><td>Fuji Speedway Hotel</td><td>Shizuoka</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Kazakhstan

#### Astana

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Kazakhstan"><td>The St. Regis Astana</td><td>Astana</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Laos

#### Luang Prabang

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Laos"><td>Amantaka</td><td>Luang Prabang</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Laos"><td>Rosewood Luang Prabang</td><td>Luang Prabang</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Malaysia

#### Bandar Penawar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Mandarin Oriental, Desaru Coast</td><td>Bandar Penawar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Johor

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Anantara Desaru Coast Resort &amp; Villas</td><td>Johor</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kuala Lumpur

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Four Seasons Hotel Kuala Lumpur</td><td>Kuala Lumpur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Mandarin Oriental, Kuala Lumpur</td><td>Kuala Lumpur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Park Hyatt Kuala Lumpur</td><td>Kuala Lumpur</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>The St. Regis Kuala Lumpur</td><td>Kuala Lumpur</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Langkawi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>Four Seasons Resort Langkawi</td><td>Langkawi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>The Ritz-Carlton, Langkawi</td><td>Langkawi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Malaysia"><td>The St. Regis Langkawi</td><td>Langkawi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Maldives

#### Baa Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Four Seasons Maldives Landaa Giraavaru</td><td>Baa Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Soneva Fushi</td><td>Baa Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Dhaalu Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>The St. Regis Maldives Vommuli Resort</td><td>Dhaalu Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Finolhas

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Amilla Maldives</td><td>Finolhas</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Laamu Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Six Senses Laamu</td><td>Laamu Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Lhaviyani

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Kudadoo Maldives Private Island</td><td>Lhaviyani</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Makunudhoo Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Soneva Secret</td><td>Makunudhoo Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Malé

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Cheval Blanc Randheli</td><td>Malé</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Jumeirah Maldives Olhahali Island</td><td>Malé</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Noonu Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Soneva Jani</td><td>Noonu Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Velaa Private Island</td><td>Noonu Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### North Ari Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>W Maldives</td><td>North Ari Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### North Malé Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Four Seasons Maldives Kuda Huraa</td><td>North Malé Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Gili Lankanfushi, Maldives</td><td>North Malé Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>One&amp;Only Reethi Rah</td><td>North Malé Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Patina Maldives, Fari Islands</td><td>North Malé Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>The Ritz-Carlton Maldives, Fari Islands</td><td>North Malé Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### South Ari Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Conrad Maldives Rangali Island</td><td>South Ari Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### South Malé Atoll

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Taj Exotica Resort &amp; Spa, Maldives</td><td>South Malé Atoll</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Maldives"><td>Waldorf Astoria Maldives Ithaafushi</td><td>South Malé Atoll</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Mongolia

#### Ulaanbaatar

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Mongolia"><td>Shangri-La Ulaanbaatar</td><td>Ulaanbaatar</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Philippines

#### Malay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Shangri-La Boracay</td><td>Malay</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pamalican Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Amanpulo</td><td>Pamalican Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Taguig

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Philippines"><td>Shangri-La The Fort, Manila</td><td>Taguig</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### South Korea

#### Busan

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>Paradise Hotel Busan</td><td>Busan</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>SIGNIEL BUSAN</td><td>Busan</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Jeju-do

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="South Korea"><td>JW Marriott Jeju Resort &amp; Spa</td><td>Jeju-do</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Sri Lanka

#### Colombo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Sri Lanka"><td>Shangri-La Colombo</td><td>Colombo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Galle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Sri Lanka"><td>Amangalla</td><td>Galle</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tangalle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Sri Lanka"><td>Amanwella</td><td>Tangalle</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Sri Lanka"><td>Anantara Peace Haven Tangalle</td><td>Tangalle</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Taiwan

#### Kaohsiung City

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>InterContinental Kaohsiung</td><td>Kaohsiung City</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Pingtung County

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Gloria Manor</td><td>Pingtung County</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Taipei

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Capella Taipei</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Grand Hyatt Taipei</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Hotel Proverbs Taipei</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Mandarin Oriental, Taipei</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Regent Taipei</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>Shangri-La Far Eastern Plaza</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Taiwan"><td>W Taipei</td><td>Taipei</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Thailand

#### Chiang Rai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Golden Triangle Elephant Camp and Resort</td><td>Chiang Rai</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Four Seasons Tented Camp Golden Triangle</td><td>Chiang Rai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Krabi

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Banyan Tree Krabi</td><td>Krabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Phulay Bay, a Ritz-Carlton Reserve</td><td>Krabi</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Rayavadee Krabi</td><td>Krabi</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Nakhon Ratchasima

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>InterContinental Khao Yai Resort</td><td>Nakhon Ratchasima</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Phang Nga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Anantara Koh Yao Yai Resort &amp; Villas</td><td>Phang Nga</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Asia" data-country="Thailand"><td>Six Senses Yao Noi</td><td>Phang Nga</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Vietnam

#### Dien Ban

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Four Seasons Resort The Nam Hai</td><td>Dien Ban</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ninh Hai

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Amanoi</td><td>Ninh Hai</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Ninh Hoa

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Six Senses Ninh Van Bay</td><td>Ninh Hoa</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Quang Ninh

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>InterContinental Halong Bay Resort</td><td>Quang Ninh</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Quy Nhon

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Asia" data-country="Vietnam"><td>Anantara Quy Nhon Villas</td><td>Quy Nhon</td><td>FHR</td><td>—</td></tr>
</tbody></table>

## Oceania

### Australia

#### Adelaide

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sofitel Adelaide</td><td>Adelaide</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Bowen Mountain

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Spicers Sangoma Retreat</td><td>Bowen Mountain</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Brisbane

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Emporium Hotel South Bank</td><td>Brisbane</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hotel X Brisbane Fortitude Valley, Vignette Collection</td><td>Brisbane</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hyatt Regency Brisbane</td><td>Brisbane</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sofitel Brisbane Central</td><td>Brisbane</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>W Brisbane</td><td>Brisbane</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Burswood

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Crown Metropol Perth</td><td>Burswood</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Cairns

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Lizard Island</td><td>Cairns</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Canberra

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hyatt Hotel Canberra - A Park Hyatt Hotel</td><td>Canberra</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Coogee

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Sydney Coogee Beach</td><td>Coogee</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Crafers

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Mount Lofty House Boutique Estate</td><td>Crafers</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sequoia - Intimate Adults Only Luxury Lodge</td><td>Crafers</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hamilton Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Sundays</td><td>Hamilton Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hayman Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Hayman Great Barrier Reef</td><td>Hayman Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hobart

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Tasman, a Luxury Collection Hotel, Hobart</td><td>Hobart</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Kingscote

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Southern Ocean Lodge, Beckons</td><td>Kingscote</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Marananga

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Louise, Beckons</td><td>Marananga</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Maryvale

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Spicers Peak Lodge</td><td>Maryvale</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Melbourne

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>1 Hotel Melbourne</td><td>Melbourne</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Crown Metropol Melbourne</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Crown Towers</td><td>Melbourne</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Grand Hyatt Melbourne</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hilton Melbourne Little Queen St</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hyatt Centric Melbourne</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hyde Melbourne Place</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Melbourne the Rialto</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Pan Pacific Melbourne</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Park Hyatt Melbourne</td><td>Melbourne</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sofitel Melbourne Collins</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Langham, Melbourne</td><td>Melbourne</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Ritz-Carlton, Melbourne</td><td>Melbourne</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The StandardX Melbourne</td><td>Melbourne</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>W Melbourne</td><td>Melbourne</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Mossman

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Silky Oaks Lodge, Beckons</td><td>Mossman</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Paddington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>25hours Hotel Sydney The Olympia</td><td>Paddington</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Palm Cove

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Reef House Adults Retreat Palm Cove</td><td>Palm Cove</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Perth

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>COMO The Treasury</td><td>Perth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Crown Towers Perth</td><td>Perth</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Pan Pacific Perth</td><td>Perth</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Ritz-Carlton, Perth</td><td>Perth</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sorrento

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Sorrento Mornington Peninsula</td><td>Sorrento</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Surfers Paradise

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>JW Marriott Gold Coast Resort &amp; Spa</td><td>Surfers Paradise</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Langham Gold Coast &amp; Jewel Residences managed by Langham</td><td>Surfers Paradise</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Sydney

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Ace Hotel Sydney</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Capella Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Crown Towers Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Four Seasons Hotel Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hilton Sydney</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Hyatt Regency Sydney</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Sydney Double Bay</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>InterContinental Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Kimpton Margot Sydney</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Park Hyatt Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Shangri-La Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sofitel Sydney Darling Harbour</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Sofitel Sydney Wentworth</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>The Porter House Hotel Sydney, MGallery</td><td>Sydney</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>W Sydney</td><td>Sydney</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Whitsundays

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Daydream Island Resort and Living Reef</td><td>Whitsundays</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Yallingup

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Smiths Beach Resort</td><td>Yallingup</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Yulara

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Australia"><td>Longitude 131, Beckons</td><td>Yulara</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### Fiji

#### Malolo Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>Six Senses Fiji</td><td>Malolo Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Natadola

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>InterContinental Fiji Golf Resort &amp; Spa</td><td>Natadola</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Pacific Harbour

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>Nanuku Resort Fiji</td><td>Pacific Harbour</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Yaukuve Levu Island

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Fiji"><td>Kokomo Private Island Fiji</td><td>Yaukuve Levu Island</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### French Polynesia

#### Arue

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>The Brando, Tetiaroa Private Island</td><td>Arue</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Bora Bora

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Conrad Bora Bora Nui</td><td>Bora Bora</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Four Seasons Resort Bora Bora</td><td>Bora Bora</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>The St. Regis Bora Bora Resort</td><td>Bora Bora</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>The Westin Bora Bora Resort &amp; Spa</td><td>Bora Bora</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Moorea

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Hilton Moorea Lagoon Resort and Spa</td><td>Moorea</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Papeete

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="French Polynesia"><td>Hilton Hotel Tahiti</td><td>Papeete</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Guam

#### Tamuning

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="Guam"><td>Dusit Thani Guam Resort</td><td>Tamuning</td><td>FHR</td><td>—</td></tr>
</tbody></table>

### New Zealand

#### Auckland

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Hilton Auckland</td><td>Auckland</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>InterContinental Auckland</td><td>Auckland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Park Hyatt Auckland</td><td>Auckland</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>SO/ Auckland</td><td>Auckland</td><td>THC</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Sofitel Auckland Viaduct Harbour</td><td>Auckland</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Christchurch

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>The George</td><td>Christchurch</td><td>THC</td><td>—</td></tr>
</tbody></table>

#### Featherston

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Wharekauhau Country Estate</td><td>Featherston</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Glenorchy

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Blanket Bay</td><td>Glenorchy</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Hawke's Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Rosewood Cape Kidnappers</td><td>Hawke&#x27;s Bay</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Matauri Bay

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Rosewood Kauri Cliffs</td><td>Matauri Bay</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Queenstown

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Eichardt&#x27;s Private Hotel</td><td>Queenstown</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>ROKI Collection Queenstown</td><td>Queenstown</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Rosewood Matakauri</td><td>Queenstown</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Tai Tapu

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Otahuna Lodge</td><td>Tai Tapu</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Taupo

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Huka Lodge, Beckons</td><td>Taupo</td><td>FHR</td><td>—</td></tr>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Kinloch Manor &amp; Villas</td><td>Taupo</td><td>FHR</td><td>—</td></tr>
</tbody></table>

#### Wellington

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Oceania" data-country="New Zealand"><td>Sofitel Wellington</td><td>Wellington</td><td>THC</td><td>—</td></tr>
</tbody></table>

## Uncertain

### Uncertain — Soufriere

#### Soufriere

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — Soufriere"><td>Rabot Hotel from Hotel Chocolat</td><td>Soufriere</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uncertain — St. John

#### St. John

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — St. John"><td>Lovango Resort + Beach Club</td><td>St. John</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uncertain — Buenaventura

#### Buenaventura

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — Buenaventura"><td>The Buenaventura Golf &amp; Beach Resort</td><td>Buenaventura</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uncertain — Cartagena

#### Cartagena

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — Cartagena"><td>Charleston Santa Teresa Cartagena Hotel</td><td>Cartagena</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uncertain — Santiago

#### Santiago

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — Santiago"><td>NH Collection Plaza Santiago</td><td>Santiago</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uncertain — Calheta

#### Calheta

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — Calheta"><td>Saccharum Resort</td><td>Calheta</td><td>THC</td><td>—</td></tr>
</tbody></table>

### Uncertain — Newcastle

#### Newcastle

<table>
<thead><tr><th>Hotel</th><th>Location</th><th>Program</th><th>Our review</th></tr></thead>
<tbody>
<tr class="hotel-row" data-region="Uncertain" data-country="Uncertain — Newcastle"><td>QT Newcastle</td><td>Newcastle</td><td>THC</td><td>—</td></tr>
</tbody></table>

