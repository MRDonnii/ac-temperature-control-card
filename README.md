# AC Temperature Control Card

Optimistisk temperaturstyring til et `climate`-kort: UI'et opdaterer sig selv med det samme når du trækker/klikker, og sender først den faktiske `climate.set_temperature`-kommando når du slipper — så det ikke spammer state-ændringer eller føles forsinket, mens Home Assistant venter på enhedens svar.

```yaml
type: custom:ac-temperature-control-card
entity: climate.stue
```

## Config

| Felt | Type | Standard |
|---|---|---|
| `entity` | entity-id | **påkrævet** — et `climate`-domæne |

## Installation

1. Kopiér `ac-temperature-control-card.js` til `/config/www/`.
2. Tilføj som Lovelace-resource: `/local/ac-temperature-control-card.js?v=1`, type `module`.
3. Tilføj kortet med din egen `entity`.
