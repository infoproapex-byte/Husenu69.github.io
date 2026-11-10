# Modificări în index.html (Husenu69.github.io)

Deschide `index.html` pe GitHub → creion (Edit) → fă modificările de mai jos → Commit changes.
Folosește Ctrl+F în editor ca să găsești textul.

## 1. Înlocuiește tot blocul JSON-LD
Găsește `<script type="application/ld+json">` ... `</script>` și înlocuiește-l cu:

```html
<script type="application/ld+json">
{
"@context": "https://schema.org",
"@type": "LocalBusiness",
"@id": "https://zoltanappliancesrepair.com/#business",
"name": "Zoltan Appliance Repair",
"url": "https://zoltanappliancesrepair.com/",
"telephone": "+1-757-817-3934",
"priceRange": "$$",
"logo": "https://zoltanappliancesrepair.com/favicon/favicon-96x96.png",
"image": "https://zoltanappliancesrepair.com/photo1.jpeg",
"description": "Appliance repair in Williamsburg, Virginia and surrounding areas.",
"address": {"@type": "PostalAddress", "addressLocality": "Williamsburg", "addressRegion": "VA", "postalCode": "23188", "addressCountry": "US"},
"openingHoursSpecification": [{"@type": "OpeningHoursSpecification", "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"], "opens": "09:00", "closes": "18:00"}],
"areaServed": [
{"@type": "City", "name": "Williamsburg"},
{"@type": "AdministrativeArea", "name": "James City County"},
{"@type": "City", "name": "Yorktown"},
{"@type": "City", "name": "Toano"},
{"@type": "City", "name": "Newport News"}
],
"hasOfferCatalog": {
"@type": "OfferCatalog",
"name": "Appliance repair services",
"itemListElement": [
{"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Refrigerator repair", "url": "https://zoltanappliancesrepair.com/refrigerator-repair-williamsburg-va/"}},
{"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Washer repair", "url": "https://zoltanappliancesrepair.com/washer-repair-williamsburg-va/"}},
{"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Dryer repair", "url": "https://zoltanappliancesrepair.com/dryer-repair-williamsburg-va/"}},
{"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Dishwasher repair", "url": "https://zoltanappliancesrepair.com/dishwasher-repair-williamsburg-va/"}},
{"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Oven and stove repair", "url": "https://zoltanappliancesrepair.com/oven-stove-repair-williamsburg-va/"}},
{"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Freezer repair", "url": "https://zoltanappliancesrepair.com/freezer-repair-williamsburg-va/"}}
]
},
"sameAs": [
"https://www.yelp.com/biz/zoltan-williamsburg",
"https://nextdoor.com/pages/zoltan-appliance-repair-williamsburg-va/",
"https://www.facebook.com/p/Zoltan-LLC-100031928273381/",
"https://www.homeadvisor.com/rated.ZoltanLLC.93759099.html"
]
}
</script>
```

## 2. Twitter Card
Sub linia `<meta property="og:image" ...>` adaugă:
```html
<meta property="og:image:width" content="1600">
<meta property="og:image:height" content="1200">
<meta property="og:image:alt" content="Zoltan Appliance Repair technician in Williamsburg, VA">
<meta name="twitter:card" content="summary_large_image">
```
(Dacă `photo1.jpeg` are altă dimensiune, schimbă cele două numere.)

## 3. Fonturi care nu blochează încărcarea
Înlocuiește linia `<link href="https://fonts.googleapis.com/css2?..." rel="stylesheet">` cu:
```html
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" media="print" onload="this.media='all'">
<noscript><link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet"></noscript>
```

## 4. Secțiunea de servicii: titlu cu cuvinte cheie + linkuri interne
Înlocuiește:
```html
<h2>What we fix</h2>
<p class="sub">Tap an appliance to see common problems we repair.</p>
```
cu:
```html
<h2>Appliance repair services in Williamsburg, VA</h2>
<p class="sub">Tap an appliance to see common problems we repair, or open its page for details.</p>
<div class="tags" style="margin-bottom:16px">
<span><a href="/refrigerator-repair-williamsburg-va/">Refrigerator repair</a></span>
<span><a href="/washer-repair-williamsburg-va/">Washer repair</a></span>
<span><a href="/dryer-repair-williamsburg-va/">Dryer repair</a></span>
<span><a href="/dishwasher-repair-williamsburg-va/">Dishwasher repair</a></span>
<span><a href="/oven-stove-repair-williamsburg-va/">Oven and stove repair</a></span>
<span><a href="/freezer-repair-williamsburg-va/">Freezer repair</a></span>
</div>
```

## 5. Zonele deservite: uniformizare + linkuri
Înlocuiește `<span>📍 North Newport News</span>` cu `<span>📍 <a href="/appliance-repair-newport-news-va/">Newport News (northern areas)</a></span>`,
`<span>📍 Yorktown</span>` cu `<span>📍 <a href="/appliance-repair-yorktown-va/">Yorktown</a></span>`,
`<span>📍 James City County</span>` cu `<span>📍 <a href="/appliance-repair-james-city-county-va/">James City County</a></span>`.

## 6. Secțiuni noi (About + FAQ)
Lipește înainte de linia `<!-- FINAL CTA -->`:
```html
<section id="about">
<h2>About Zoltan Appliance Repair</h2>
<p class="sub">Zoltan Appliance Repair is based in Williamsburg, VA. We repair refrigerators, washers, dryers, dishwashers, ovens and freezers in homes across Williamsburg, James City County, Yorktown, Toano and northern Newport News. You pay a $120 service call for the diagnosis, then you get a clear estimate for parts and labor. You decide whether to go ahead.</p>
<!-- Adaugă aici DOAR ce este adevărat: ani de experiență, licență, asigurare, garanție la reparații. -->
</section>

<section id="faq">
<h2>Frequently asked questions</h2>
<details><summary><span>How much does a service call cost?</span></summary><p>The service call and diagnostic fee is $120. We come to your home, inspect the appliance and identify the problem. Parts and labor are quoted separately.</p></details>
<details><summary><span>Do you start repairs without asking?</span></summary><p>No. We explain the repair and the price first, and we do not start any work until you say yes.</p></details>
<details><summary><span>What areas do you serve?</span></summary><p>We are based in Williamsburg, VA and serve Williamsburg, James City County, Yorktown, Toano and northern Newport News. Call (757) 817-3934 to confirm your address.</p></details>
<details><summary><span>Which appliances and brands do you repair?</span></summary><p>We repair refrigerators, washers, dryers, dishwashers, ovens, stoves and freezers from major brands including LG, Samsung, Whirlpool, GE, Bosch, Maytag, Frigidaire, KitchenAid, Kenmore, Electrolux and Amana.</p></details>
<details><summary><span>What are your hours?</span></summary><p>Monday to Friday, 9 AM to 6 PM Eastern Time. We are closed on Saturday and Sunday. Call during business hours to schedule.</p></details>
</section>
```

## 7. Poze (opțional, dar recomandat)
1. Comprimă pozele pe squoosh.app (WebP sau JPEG, sub ~200 KB fiecare).
2. Redenumește-le descriptiv, de ex. `zoltan-appliance-repair-williamsburg-1.jpeg`.
3. Actualizează numele în `index.html` (4 poze în secțiunea „See our work" + `og:image` + `image` din JSON-LD) și în paginile noi (`og:image` folosește `photo1.jpeg`).
4. Schimbă `alt` din „Zoltan repairing an appliance" în ceva specific, doar dacă poza arată ceea ce scrie.
