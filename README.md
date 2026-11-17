# synth-audio

Additive-synthesis audio parameter blobs for a runtime music system.

Each `songs/<id>.bin` encodes one track as sine + noise-band envelopes
(no audio samples are stored). Per frame: 56×uint16 partial frequencies,
then 56×uint8 amplitudes, then 3×uint8 noise-band amplitudes (little-endian).
See `manifest.json` for `K`, `fps`, `frameBytes`, and per-id frame counts.

Served over CDN via jsDelivr:

    https://cdn.jsdelivr.net/gh/<user>/<repo>@main/songs/<id>.bin
