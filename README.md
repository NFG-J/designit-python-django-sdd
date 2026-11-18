# DesignIT – Python, Django og SDD

Komplett statisk kursnettsted med ti moduler på norsk og engelsk.
Norsk er startside. Engelsk ligger i `en/`. Språklenker finnes øverst på sidene.

## Last opp til GitHub

1. Pakk ut ZIP-filen på datamaskinen.
2. Opprett et nytt repository på GitHub, for eksempel `designit-python-django-sdd`.
3. Velg **Add file → Upload files** og last opp **innholdet** i den utpakkede mappen. `index.html` skal ligge direkte i roten av repoet. Behold undermappen `en/`.
4. Lagre med **Commit changes**.

ZIP-filen skal pakkes ut før opplasting. En ZIP-fil som lastes opp alene blir ikke et publisert nettsted.

## Publiser med GitHub Pages

1. Åpne repoets **Settings → Pages**.
2. Under **Build and deployment**, velg **Deploy from a branch**.
3. Velg grenen **main** og mappen **/ (root)**, og lagre.
4. Når publiseringen er ferdig, åpne nettadressen GitHub viser på Pages-siden.

Vanlig adresse er `https://DITT-BRUKERNAVN.github.io/REPO-NAVN/`.
Engelsk versjon ligger på samme adresse med `en/` til slutt.
Tilgjengeligheten av Pages for private repoer avhenger av GitHub-abonnementet.

## Kjør lokalt

Åpne `index.html` direkte i nettleseren, eller start en lokal webserver fra mappen:

```bash
python -m http.server 8000
```

Åpne deretter `http://localhost:8000`. En lokal webserver gir best støtte for nettleserfunksjoner som kopiering til utklippstavlen.

## Innhold

- `index.html`: hele det norske kurset, med innebygd CSS, JavaScript og modulinnhold.
- `course.json`: norsk modulinnhold i et separat dataformat.
- `spec-mal.md`: norsk spesifikasjonsmal.
- `en/index.html`: hele det engelske kurset.
- `en/course.json`: engelsk modulinnhold.
- `en/spec-template.md`: engelsk spesifikasjonsmal.
- `.nojekyll`: nettstedet publiseres som vanlige statiske filer.

Ingen npm-installasjon eller byggetrinn er nødvendig. Progresjon lagres i studentens nettleser, separat for hvert språk. Ingen server eller database trengs for selve kursnettstedet. Python-/Django-koden i modulene er øvingskode som studentene kjører separat; GitHub Pages kjører ikke Django.

## Redigere kurset

Modulene som vises på nettsidene, finnes i JavaScript-variabelen `modules` i hver `index.html`. Rediger den relevante HTML-filen når du endrer kurset. De separate JSON-filene lastes ikke automatisk inn av nettsiden; hold dem oppdatert hvis du bruker dem til videre bearbeiding. CSS ligger i `<style>` og funksjonaliteten i `<script>`.

Kurssidene kan også laste ned HTML-kopi og spesifikasjonsmal direkte fra nettleseren.

## Opphav og kilde

Eksport av DesignIT-kurssidene, 17. november 2026:

- Norsk: https://designit-python-django-lynkurs.designit-4594.chatgpt.site
- Engelsk: https://designit-python-django-english.designit-4594.chatgpt.site

Denne pakken legger ikke til en ny lisens. Bruk prosjektets avtalte rettigheter og lisensvilkår ved videre deling.
