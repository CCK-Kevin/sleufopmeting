# Sleufopmeting CCK — zelfstandige versie

Statische web-app (geen build nodig). Werkt op iPhone, iPad, Android en laptop.

## Bestanden
| Bestand | Waarvoor |
|---|---|
| `index.html` | De volledige app |
| `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png` | Op beginscherm zetten met eigen icoon, schermvullend openen |
| `sw.js` | Offline: na één keer openen start de app ook zonder bereik |
| `vercel.json` | Zorgt dat updates meteen doorkomen (geen oude versie in cache) |

## Op Vercel zetten
**Via GitHub (aanbevolen):**
1. Maak een nieuwe repository (bv. `sleufopmeting`) en zet deze map erin.
2. Vercel → *Add New… → Project* → kies de repository.
3. Framework Preset: **Other**. Build Command: leeg. Output Directory: leeg (root).
4. *Deploy*. Je krijgt een adres als `sleufopmeting.vercel.app`.

**Via de terminal:** in deze map `npx vercel --prod`.

Een update = `index.html` vervangen en opnieuw pushen/deployen.

## Op de gsm of iPad
- **iPhone/iPad:** open het adres in **Safari** → Deel → **Zet op beginscherm**.
- **Android:** open in Chrome → menu ⋮ → **App installeren** / Toevoegen aan startscherm.

## Gegevens
- Alles wordt **op het toestel zelf** bewaard (geen server). Iedereen met de link kan de app openen, maar ziet enkel zijn eigen gegevens.
- Project naar een ander toestel: Menu → **Project exporteren** → bestand doorsturen → op het andere toestel Menu → **Project importeren**.
- Gegevens uit de Claude-versie overzetten: daar *Project exporteren*, hier *Project importeren*.
- Op iPhone/iPad wist Safari websitegegevens na 7 dagen zonder gebruik — **zet de app op het beginscherm**, dan geldt dat niet.
