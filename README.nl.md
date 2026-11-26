# SceneRadio M3U

[English](README.md) · **Nederlands**

Een automatisch bijgewerkte M3U-lijst met Nederlandse landelijke, regionale en DAB+-radiostations, met logo's. Gemaakt voor de Android-app **SceneRadio**, maar te gebruiken in elke speler die M3U-lijsten met `tvg-logo` en `group-title` kent.

## Gebruik

Het adres van de lijst:

```
https://raw.githubusercontent.com/onneau/sceneradio-m3u/main/nederlandse-radio.m3u
```

- **SceneRadio**: de lijst is de standaardlijst. Er is geen account of token nodig.
- **Andere spelers**: voeg het adres hierboven toe als afspeellijst of "M3U-URL".
- De logo's staan in `logos/` en worden in de lijst relatief genoemd (`tvg-logo="logos/<naam>.jpg?v=<code>"`). Spelers die relatieve adressen niet begrijpen, plakken er `https://raw.githubusercontent.com/onneau/sceneradio-m3u/main/` voor.
- GitHub bewaart raw-bestanden een paar minuten in de cache, dus een nieuwe versie kan even duren.

## Wat staat erin

| Bestand | Inhoud |
| --- | --- |
| `nederlandse-radio.m3u` | de lijst: naam, genres (`group-title`, meerdere gescheiden door `;`), logo en stream-adres |
| `logos/*.jpg` | logo's, hoogstens 500 punten aan de langste zijde |
| `logos/manifest.json` | per logo de bron waar het vandaan komt |

## Hoe de lijst wordt gemaakt

Deze repository bevat alleen het **resultaat**. De lijst wordt automatisch gemaakt en gecontroleerd in een aparte, eigen bronlijst:

- Streams worden dagelijks gecontroleerd. Een zender valt pas uit de lijst na drie keer achter elkaar een fout, en komt vanzelf terug zodra de stream weer werkt.
- Logo's komen van Wikimedia Commons, van de zenders zelf of van de [Radio Browser](https://www.radio-browser.info)-database.
- Wijzigingen in deze repository worden door de beheerder gemaakt; losse wijzigingen hier worden bij de volgende update overschreven.

## Een zender mist of werkt niet?

Maak een *issue* aan met de naam van de zender en, als je die hebt, het adres van de stream.

## Geen verband met de zenders

Dit project is op geen enkele manier verbonden aan, gesponsord door of goedgekeurd door de radiozenders, omroepen of bedrijven waarvan de naam, het logo of de stream in de lijst voorkomt. Alle namen en logo's zijn eigendom van hun eigenaren en worden alleen gebruikt om een zender herkenbaar te maken. Er staat **geen audio** in deze repository: de streams worden rechtstreeks bij de zenders opgehaald.

**Wil een rechthebbende dat een naam, logo of stream hier verdwijnt?** Meld dat via een *issue* of via https://github.com/onneau. Het wordt dan zo snel mogelijk verwijderd.

## Licentie

De lijst en de teksten vallen onder de [PolyForm Noncommercial License 1.0.0](LICENSE): gebruik voor privé, hobby, onderzoek, onderwijs en goede doelen, niet commercieel. Zie `NOTICE.nl.md` ([English](NOTICE)) voor wat daar niet onder valt (de logo's en namen van de zenders).
