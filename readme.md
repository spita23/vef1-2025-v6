# Vefforritun 1, 2025: Verkefni 6, CSS/Tæki&tól #4

**Athugið að þessu verkefni þarf að skila með vísun í GitHub.**

## Markmið

- Setja upp Node.js og NPM og nota til að sækja pakka.
- Nota tól fengin af NPM.
- Keyra tól í vinnuflæði með `package.json`.

## Verkefni 2–6

Í verkefnum 2–6 munum við vinna áfram með sama verkefni og byggja ofan á það:

- [Verkefni 2](https://github.com/vefforritun/vef1-2025-v2) skilgreinir grunn HTML og síður.
- [Verkefni 3](https://github.com/vefforritun/vef1-2025-v3) bætir við grunn viðmóti.
- [Verkefni 4](https://github.com/vefforritun/vef1-2025-v4) setur upp skipulagðra útlit.
- [Verkefni 5](https://github.com/vefforritun/vef1-2025-v5) setur upp grind og gerir útlit skalanlegt (e. responsive).
- [Verkefni 6](https://github.com/vefforritun/vef1-2025-v6) setur upp tól til að hjálpa við skipulag og vinnu.

## Lýsing

Verkefnið er framhald af [verkefni 2](https://github.com/vefforritun/vef1-2025-v2), [verkefni 3](https://github.com/vefforritun/vef1-2025-v3), [verkefni 4](https://github.com/vefforritun/vef1-2025-v4) og [verkefni 5](https://github.com/vefforritun/vef1-2025-v5), nýtir það efni sem uppsett er í því, og fylgir þeirri verkefnalýsingu. Leyfilegt er að nota sýnilausnir: [sýnilausn að verkefni 4](https://github.com/vefforritun/vef1-2025-v4-synilausn) eða [sýnilausn að verkefni 5](https://github.com/vefforritun/vef1-2025-v5-synilausn) sem gefin verður út föstudaginn 26. september.

## Grunnur

Gefið er `styles.scss` (ath _scss_ ekki _css_) skjal með grunn að lausn og vísun í aðrar skrár í `styles/` möppunni. Skjalið er með athugasemdum svipað og í verkefnum 3–5. Sama og gilti almennt þar gildir áfram.

Athugið að til þess að þetta virki þarf að setja upp Parcel með Sass stuðningu.

## Útlit

Sama gildir og í verkefni 5 en útlit er samt ekki markmið í þessu verkefni.

## Takmarkanir

Leyfilegt er að nota allt CSS og Sass virkni.

## Tæki og tól

Til þess að geta notað þessi tól þarf að [setja upp Node.js, sækið „Recommended For Most Users“](https://nodejs.org/en/). Eftir að þið hafið keyrt uppsetningar forrit getið þið opnað Command prompt/terminal/skel og keyrt:

```bash
> node -v
v22.19.0 # eða sú útgáfa sem þið sóttuð
> npm -v
10.9.3 # eða álíka
```

Ef þið fáið þetta ekki upp, prófið að endurræsa. Annars fá aðstoð í dæmatímum, í fyrirlestri, tölvupósti eða á slack.

Fyrst þarf að búa til `package.json` með því að keyra `npm init` í verkefnamöppu. Sjá dæmi í tíma 22. september 2025.

### Sass

Nota skal `./styles.scss` (gefin) sem grunn Sass skrá sem vísar í allar aðrar. Skipta skal CSS upp í mismunandi skrár undir `styles/`. Skipta skal verkefninu upp í að minnsta kosti 10 skrár. Þar með talið:

- `config.scss` – stillingar, breytur.
- `reset.scss` – endurstilla vafra sjálfgefna stíla.
- `base.scss` – grunn stílar.
- `grid.scss` – grind til aðstoðar, sjá gefinn grunn.
- `utils.scss` – hjálparklasa (e. utility classes).
- `components/` – stílar fyrir hluta (e. components) eins og haus, fót, kort.

Í `styles/config.scss` skal geyma allar stillingar fyrir verkefni og nota þær á viðeigandi stöðum.

### Parcel

Setja skal verkefnið upp með [Parcel](https://parceljs.org/), sjá dæmi í tíma 22. september 2025. Parcel hefur [innbyggðan Sass stuðning](https://parceljs.org/languages/sass/).

Setja þarf upp `dev` og `build` script í `package.json` til að keyra Parcel, [sjá skjölun](https://parceljs.org/getting-started/webapp/#package-scripts). Það gæti verið ráð að setja `dev` script með `--no-cache` og `--lazy` valkostum til að forðast vandamál með cache:

```text
"dev": "parcel index.html 'sidur/*.html' --lazy --no-cache"
```

### Linting

Setja skal upp stylelint með `npm create stylelint@latest` og síðan setja upp `stylelint-config-standard-scss` og `stylelint-config-recess-order`.

`stylelint.config.mjs` skal þá innihalda:

```js
/** @type {import("stylelint").Config} */
export default {
  extends: ["stylelint-config-standard-scss", "stylelint-config-recess-order"],
};
```

Þegar skipunin `npm run lint` er keyrð skal keyra stylelint með þessum reglum og ættu engar villur að koma fram.

Athugið að hægt er að keyra `stylelint` með `--fix` til að laga sumar villur sjálfkrafa.

Gefið er `.stylelintrc` skjal sem inniheldur hunsar `dist/` möppu.

### GitHub & Netlify

Setja skal upp verkefnið á GitHub og skila með slóð á repo. Tengja skal Netlify við GitHub repo.

Gefið er `.gitignore` skjal sem útilokar `node_modules/` og `dist/` möppur, þetta skjal verður að vera til staðar.

## Mat

- 30% – CSS flutt yfir í Sass
- 30% – stylelint uppsett og engar villur
- 30% – Verkefni sett upp með git, repo á GitHub og tengt þaðan við Netlify
- 10% – Verkefni sett upp með `package.json` og viðeigandi scriptum

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 22. september 2025.

## Skil

Skila skal í Canvas, seinasta lagi fyrir lok dags fimmtudaginn 2. október 2025.

Skilaboð skulu innihalda:

- Slóð á verkefnið keyrandi í hýsingu
- Slóð á GitHub repo fyrir verkefni. Dæmatímakennurum skal hafa verið boðið í repo. Notendanöfn þeirra eru:
  - `klingsterina`
  - `kristinfrida`
  - `osk`
  - `reynirjr`

## Aðstoð

Leyfilegt er að ræða, og vinna saman að verkefni en **skrifið ykkar eigin lausn**. Ef tvær eða fleiri lausnir eru mjög líkar þarf að færa rök fyrir því, annars munu allir hlutaðeigandi hugsanlega fá 0 fyrir verkefnið.

Ekki er heimilt að nota stór mállíkön til að vinna verkefni í námskeiðinu, [sjá nánar um notkun](https://github.com/vefforritun/vef1-2024/blob/main/mallikon.md).

## Verkefni og einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 5% hvert, samtals 40% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 10%, samtals 20% af lokaeinkunn.

> Útgáfa 0.1

## Útgáfusaga

| Útgáfa | Lýsing                     |
| ------ | -------------------------- |
| 0.1    | Fyrsta útgáfa verkefnisins |
