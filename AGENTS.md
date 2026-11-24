# OpenDepthMap Hardware & Firmware Governance Guardrails

## Visibility Tier: TIER 3 - PUBLIC OPEN HARDWARE & FIRMWARE (ORGANIZATION)
- Target remote: `github.com/opendepthmap/hardware` (Public).
- Licensing: CERN-OHL-P v2 for CAD, STL, schematics, and BOMs; MIT for embedded firmware.

## Hard Boundary Rules
- Keep this repository strictly scoped to open hardware designs, documentation, and embedded firmware. Never commit closed-source services, internal infrastructure, private notes, or credentials.
- NEVER commit local Wi-Fi credentials, device API keys, or OAuth tokens.
- Keep documentation and public interface descriptors free of em dashes.

## Standard Build Commands
- Firmware (ESP32-S3 / ESP32-C3): `pio run` (Compiles PlatformIO firmware targets)

## Human-Factors & Hardware Safety Guardrails
- Always enforce the three-stage telemetry freshness state machine (`FIX: LIVE` 0-5s, `LAG` 6-30s, `STALE` >30s) and minimal compass/depth watchdog fallback screen on the diver wrist receiver.
- Preserve dual-bank OTA rollback (`OTA_0`/`OTA_1`) on ESP32 targets and read-only overlay with A/B switching on Raspberry Pi targets.
- Wire frame formats and `opendepthmap.local` payloads MUST conform to the public schemas published in `opendepthmap/protocols`.
