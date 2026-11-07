# DIFFERENCE — Cyber Security & Digital Protection

Premium dark prezentacijska web stranica za DIFFERENCE, obrt za usluge, uz očuvanu edukacijsku aplikaciju. Statički HTML/CSS/JS, bez build koraka i bez obveznih vanjskih skripti.

## Lokalni pregled

```bash
python3 -m http.server 8000
```

Otvorite http://localhost:8000.

## Netlify

- Build command: ostaviti prazno.
- Publish directory: `.`
- `netlify.toml` već sadrži sigurnosna zaglavlja i nema više wildcard SPA preusmjeravanja.
- Kontaktni obrazac koristi Netlify Forms (`data-netlify="true"`). Nakon prvog deploya provjerite da je obrazac prepoznat u Netlify Forms i pošaljite testni upit.
- Netlify Forms mora biti uključen u postavkama projekta. Provjerite obavijesti i primatelja za zaprimljene upite.

## Domena i SEO — potrebno dovršiti nakon odabira domene

Domena još nije odabrana. Namjerno nisu upisani lažni canonical URL-ovi niti izmišljena sitemap domena. Nakon odabira domene:
1. Povežite domenu s Netlify projektom i provjerite HTTPS.
2. Dodajte canonical URL na svaku HTML stranicu.
3. Izradite `sitemap.xml` s apsolutnim URL-ovima svih javnih stranica.
4. U `robots.txt` dodajte `Sitemap: https://ODABRANA-DOMENA/sitemap.xml`.
5. Dodajte domenu u Google Search Console.
6. Ako se mijenjaju stare putanje, dodajte pojedinačna 301 preusmjeravanja.

## Kontaktni obrazac

Obrazac je pripremljen za Netlify Forms. Provjerite funkcionalnost nakon deploya. Nemojte u obrazac tražiti lozinke, PIN-ove, jednokratne kodove ili osjetljive dokumente. Uključite spam zaštitu i ograničite pristup zaprimljenim upitima.

## Cijene

Cijene nisu izmišljene. Kartice prikazuju predložene pakete, ali iznosi su označeni kao „Cijena uskoro” dok vlasnik ne potvrdi stvarni cjenik, sadržaj paketa i eventualne troškove licenci/putovanja. Ne objavljivati kao konačan cjenik prije popunjavanja.

## Pravne stranice — obvezna provjera prije javne objave

Dokumenti su početni nacrti, ne pravno mišljenje. Prije objave provjeriti registrirani naziv i djelatnosti, stvarne pružatelje obrade (Netlify i drugi), pravnu osnovu, rokove čuvanja, potrošačke informacije, pravo na raskid, porezni status i način ugovaranja.

## Edukacija

Postojeći edukacijski sadržaj premješten je u `/edukacija/`, zajedno s `app.js`, `styles.css` i `data/content.json`. Sačuvano je 26 sadržajnih cjelina i 54 vježbe. Aplikacija koristi localStorage; spremljeni podaci iz stare aplikacije mogu biti vezani uz prethodni origin i putanju. Korisnici bi trebali izvesti ili sačuvati bilješke prije migracije ako je prethodna verzija već korištena.

## Poslovni podaci uneseni u projekt

- DIFFERENCE, obrt za usluge
- Martićeva 67, Zagreb
- OIB: 58245272280
- Telefon: +385 95 8280 800
- E-mail: difference.usluge@gmail.com

IBAN i BIC nisu prikazani javno.

## Kontrolna lista prije objave

- [ ] Potvrditi konačnu domenu.
- [ ] Definirati iznose i točan opseg paketa.
- [ ] Provjeriti registrirane djelatnosti i pravne dokumente.
- [ ] Provjeriti Netlify Forms nakon deploya.
- [ ] Provjeriti obavijesti o novim upitima.
- [ ] Dodati canonical URL-ove i sitemap nakon izbora domene.
- [ ] Provjeriti sve linkove, mobilni prikaz i stvarni sadržaj.
- [ ] Povezati Search Console i po želji analitiku uz odgovarajuću privolu.


## Nova domena i BrandistiQ potpis (verzija 1.2)

Primarna domena projekta je **https://digitalna-sigurnost.com.hr/**. Sve glavne HTML stranice imaju canonical i Open Graph URL za tu domenu, a dodan je i `sitemap.xml` te ažuriran `robots.txt`.

Na dnu svake stranice nalazi se klikabilni BrandistiQ logo uz oznaku **POWERED BY**. Logo vodi na https://brandistiq.eu. Edukacijska aplikacija ima zaseban footer potpis jer koristi vlastiti raspored i CSS.

### Obavezno prije produkcije
1. U Netlify projektu otvoriti **Domain management → Add a domain** i dodati `digitalna-sigurnost.com.hr` te `www.digitalna-sigurnost.com.hr`.
2. Kod registrara domene postaviti DNS zapise točno prema vrijednostima koje prikaže Netlify (nemoj nasumično mijenjati postojeće nameservere ili A/CNAME zapise).
3. U Netlifyju postaviti `digitalna-sigurnost.com.hr` kao primary domain i provjeriti izdavanje HTTPS certifikata.
4. Nakon što domena radi preko HTTPS-a, u Google Search Console dodati domenu ili URL-prefix property i poslati `https://digitalna-sigurnost.com.hr/sitemap.xml`.
5. Provjeriti kontaktni Netlify Forms obrazac nakon produkcijskog deploya.

Preusmjeravanje `www` na glavnu domenu uključeno je u `netlify.toml`; stvarno će raditi tek nakon što su obje domene dodane Netlify projektu i DNS ispravno postavljen.
