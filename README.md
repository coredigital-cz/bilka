# BilkaRoofArt — site (bazat pe codul/designul ADC)

## Înainte de publicare
Înlocuiește `DOMENIUL-TAU.ro` cu domeniul real, în `index.html`, `404.html`,
`robots.txt` și `sitemap.xml`:

    sed -i 's/DOMENIUL-TAU\.ro/domeniul-real.ro/g' index.html 404.html robots.txt sitemap.xml

## Ce s-a schimbat față de site-ul original (ADC)
- **Brand**: "ADC Acoperisuri de Calitate" → "BilkaRoofArt" peste tot (title, meta, JSON-LD, footer, nav)
- **Logo**: SVG inline (fără fișier extern) — cel vechi (`adc-logo.jpg`) avea "ADC" scris direct pe imagine, nu putea fi refolosit
- **Telefon**: `0747 343 402` → `0721 001 888`, peste tot (tel:, wa.me, JSON-LD)
- **Ani experiență**: 25+ → 20+ (toate aparițiile: hero, intro, stats band, meta descriptions)
- **Locație**: Constanța/București/Ilfov → acoperire națională (meta geo, JSON-LD address/areaServed, hero, footer, hartă)
- **Facebook**: eliminat complet — butonul flotant, statistica "4.8K urmăritori", link-ul din JSON-LD `sameAs`. Înlocuit statul cu "500+ Proiecte finalizate"
- **Google Ads tracking**: eliminat (era contul de conversii al lui ADC, nu se aplică)
- **Poze excluse** (cerute explicit): `adc-masina.jpg`, `adc-logo.jpg`, `tigla-detaliu.jpg`, `velux-montaj.jpg` — înlocuite cu alte poze din același set (`casa-completa.jpg`, `velux-lateral.jpg`, `bilka-clasic.webp`, `izolatie-deschidere.jpg`)
- **Secțiune nouă: Parteneri** — 4 branduri (Bilka, Lindab, Wetterbest, Velux), plasată după secțiunea Bilka
- **Video testimoniale** — primele 2 din cele 3 trimise, integrate în secțiunea de recenzii, cu buton play custom
- **Favicon nou** — SVG generic (roof icon), cel vechi avea tot "ADC" pe el

## Ce a rămas neschimbat
- Codul (GSAP, ScrollTrigger, cursor custom, grain effect, marquee, hero slideshow, lightbox portofoliu)
- Toate cele 9 modele de țiglă Bilka (poze + specificații tehnice)
- Structura completă de secțiuni: hero, servicii, feature blocks, Bilka, parteneri (nou), stats, proces, portofoliu, beneficii, recenzii (+ video, nou), CTA, contact, footer
- Recenziile text (6 recenzii) — sunt generice, fără nume/detalii legate de ADC

## Deploy (Vercel + GitHub)
1. Creezi un repo nou pe GitHub, urci tot conținutul acestui folder
2. Vercel → Add New Project → Import repo → Framework Preset: **Other** (fără build command)
3. Settings → Domains → adaugi domeniul real
4. Nu uita pasul de mai sus (`sed` pe domeniu) înainte de push
