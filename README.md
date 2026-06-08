# mudum-vizualizace

Rendery PLUS domů MUDUM (Erdol 1 XL / 2 / 2 XL / 102 PLUS) pro konfigurátor.
Zdroj: erdolhaus.pl. Obrázky jsou organizované do složek podle modelu:

```
E1XLPLUS/<file>.jpg
E2PLUS/<file>.jpg
E2XLPLUS/<file>.jpg
E102PLUS/<file>.jpg
```

Soubory končí na `_W1.jpg` (předek) a `_W2.jpg` (zadek).

## Servírování přes jsDelivr



```
https://cdn.jsdelivr.net/gh/dsikling/mudum-vizualizace@main/<MODEL>/<file>.jpg
```

Příklad:
```
https://cdn.jsdelivr.net/gh/dsikling/mudum-vizualizace@main/E1XLPLUS/L_BOD_OS_OS_A_BR_W1.jpg
```

Pozn.: `@main` jsDelivr cachuje ~12 h. Pro produkci je lepší použít tag/release
(`@v1`), aby se daly verze řídit a invalidovat cache.

## JSON mapa pro konfigurátor

Mapování `config-klíč → {front, back, model}` s jsDelivr URL je vygenerované
ve zdrojovém projektu (`plus_render_export/PLUS_ALL.json`).
Klíč odpovídá sloupci `Name` v import CSV, např.:

```json
"E1XLPLUS-L_BOD_OS_OS_BOP_A_BPV_BR": {
  "model": "Erdol 1 XL PLUS",
  "front": "https://cdn.jsdelivr.net/gh/dsikling/mudum-vizualizace@main/E1XLPLUS/L_BOD_OS_OS_A_BR_W1.jpg",
  "back":  "https://cdn.jsdelivr.net/gh/dsikling/mudum-vizualizace@main/E1XLPLUS/L_OS_OS_BOP_A_BPV_BR_W2.jpg"
}
```
