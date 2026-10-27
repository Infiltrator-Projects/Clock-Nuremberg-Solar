# Nuremberg Style Solar Clock — computational and historical model

| Field | Value |
| --- | --- |
| Stable provider ID | `nuremberg-solar` |
| Resource kind | `clock` |
| Canonical compiled name | `Nuremberg Style Solar Clock.so` |
| Intended installation | `/System/Resources/Clocks/Nuremberg Style Solar Clock.so` |

## Maintained model

Location-aware modern sunrise/sunset reconstruction of a Nuremberg-style seasonal clock.

## Historical scope / fidelity limitation

**Implemented interpretation:** Nuremberg-style solar reconstruction.

**Fidelity boundary:** Deliberately distinct from the fixed historical Wendetag schedule.

This is an account of the implemented model, not a claim that a particular mathematical projection was observed or officially used in every historical period. Where the source model uses approximations, retrospective continuation or external ICU/CLDR authorities, that distinction must remain explicit.

## Observable behaviour

The clock owns both its notation and next-visible-tick scheduling. Its output needs valid geographic coordinates; missing/invalid coordinates are unavailable, not an implicit Greenwich location. Undefined solar crossings at extreme latitudes must be reported as unavailable rather than invented.

## Unsupported inputs and reproducibility

Missing providers are unavailable; consumers must not substitute a different provider with a similar name. Malformed or out-of-range inputs must return an explicit failure without modifying outputs. Module metadata must convey its true ID and kind, independent of filename ordering.

## Provenance

The model and boundary above are documented from the current resource build map, Calendar model matrix and Common historical-fidelity audit. They have not yet been independently requalified in this repository.

- [Libraries/Common temporal sources](https://github.com/Infiltrator-Projects/Libraries/tree/main/resources/temporal)
- [Current canonical build catalogue](https://github.com/Infiltrator-Projects/Libraries/blob/main/resources/temporal/Makefile)
- [Calendar chronology and clock models](https://github.com/Infiltrator-Projects/Calendar/blob/main/docs/MODELS.md)
- [Historical fidelity audit](https://github.com/Infiltrator-Projects/Libraries/blob/main/docs/TEMPORAL_HISTORICAL_FIDELITY.md)
- [Temporal discovery and executable provider ABI](https://github.com/Infiltrator-Projects/Libraries/blob/main/docs/TEMPORAL_PROVIDERS.md)
