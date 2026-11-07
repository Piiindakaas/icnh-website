# ICNH_ website

Statische one-pager voor ICNH_ (communicatie voor cyber), gehost op GitHub Pages.

## Privacy eerst

Er komt geen persoonlijke informatie in git: geen achternamen, accountgegevens,
Figma-keys, namen van andere bedrijven of interne context. Dat geldt voor bestanden,
commitberichten en PR-beschrijvingen. Zulke context staat in `CLAUDE.local.md`
(staat in `.gitignore`). Twijfel je of iets erin mag: niet committen, eerst vragen.

Uitzondering is de content van de site zelf in `index.html` en
`.well-known/security.txt`: wat daar staat, is bewust publiek.

## Structuur

- `index.html` — alle content (Engels). Elke sectie heeft een commentaar `<!-- 0X Naam -->`.
- `assets/css/style.css` — opmaak; kleuren en fonts als tokens bovenaan `:root`.
- `assets/img/` — logo's, favicon, portret, og-image.
- `.well-known/security.txt` — contactgegevens voor securityonderzoekers; `Expires` jaarlijks verlengen.
- `.github/workflows/pages.yml` — elke push naar `main` gaat automatisch live.

Geen build-stap, geen framework, geen npm. Houd het zo.

## Werkwijze bij een wijzigingsverzoek

Bijvoorbeeld "pas de tekst bij Crisis aan" of "voeg een sectie toe". Dan:

1. `git switch main && git pull`, daarna een branch: `wijziging/<korte-omschrijving>`.
2. Pas alleen aan wat gevraagd is. Content-wijzigingen raken alleen `index.html`;
   het design (kleuren, fonts, maten) alleen als daar expliciet om gevraagd wordt.
3. Preview in het browserpaneel, op desktop én mobiel (375px).
4. Commit, push, en open een PR met `gh pr create` met een korte Nederlandse omschrijving
   van wat er zichtbaar verandert.
5. Geef de PR-link. Piiindakaas merget; ~1 minuut later staat het live.

Merge nooit zelf naar `main` tenzij daar in de sessie expliciet om gevraagd wordt.

## Schrijfstijl

Teksten in de stem van Piiindakaas: direct, informeel, ik-vorm, geen marketingjargon.
Placeholders staan tussen `[HAKEN]`; verzin nooit feiten, cijfers of klantnamen.
